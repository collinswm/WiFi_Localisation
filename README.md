# UBIQUM WIFI LOCALISATION PROJECT
Ubiqum 4: Using WAP signals to detect user/phone locations across three buildings

HOW TO NAVIGATE THIS FILE:

The wifi localisation project objective is to use regression and/or classification algorithms to make predictions of the location of users and mobile phones within three large multi floor buildings. Because of the challenges of locating mobile signals indoors, a series of 520 Wireless Access Points are used. 

The project has a series of iterations. Following an initial data exploration which is not included here, there are 3 main iteration steps. there are several common parts to each script and a lot of duplication. This is intentional to allow files to easily be copied and iterated with minimal manual changes.

Iteration 1:
============
This iteration is the first attempt to make predictions. 

Step 1: Predict Building Number using classification models
Step 2: Predict Building Number and Floor Number combined using a new feature also using classification models
Step 3: Predict Floor Number for Building 0, 1 and 2 using classification models
Step 4: Predict Longitude and Latitude for all buildings (not separately) using regression models

All errors are consolidated at the end of each model and presented in simple visualisations. 

Iteration 2:
============
This iteration attempts to make more intelligent predictions focusing on cleaner WAP signals and looking at specific Longitude and Latitude per building.

Step 1: Understand WAP data and isolate high quality signals based on Var != 0
Step 2: Enhanced visualisation of user and phone IDs per building to understand where noise exists
Step 3: Predict Lat and Long for Building 0, 1 and 2 using classic regression models
Step 4: Enhanced error metric reporting and visualisation to understand the basis for issues in the models and data


Iteration 3:
============
This is effectively the final iteration. It aims to drill into Floor prediction using classification models again but this time focusing on the users where the WAP signals are considered more reliable. Here the WAP data are also normalised. 

Step 1: Undertand the value counts in data set for all buildings, floors, user, phones
Step 2: Isolate the high quality WAP signals as the basis for exploration and prediction
Step 3: Visualise User and Phones to see where noise may exist in the data reliabiity
Step 4: Normalise the WAP data (three methods attempted, scikit learn Normalizer function used) 
Step 5: Reconstitude the tables and build predictions models
Step 6: Predict Floor Number for Buildings 0, 1 and 3
Step 7: Predict Floor Number in Building 0 for User 1 and User 11 separately
Step 8: Predict Floor Number in Building 1 and 2 for all Users excluding User 14
Step 9: Present errors for each model in consolidated dataframe and scatterplot. 

Remaining work to be done:
==========================
When time permits;
1. Identify whether data is biased towards specific floors 
2. Predict based on Phone IDs and User IDs combined
3. Map predictions to Validation data to check for overfitting or underfitting
4. Refine and improve visualisations
5. Remove duplicate code and replace with functions

