# Neural_Network_Charity_Analysis

## Overview of Project

This analysis is being conducted in order to see if a significant correlation exists between the variables collected in the data about the funding applicants (type of organization, type of funding, amount of funding, etc.) and if the recipients went on to success. We will be using a neural network to attempt to create a predicitve model that could be utilized on future applicants to determine if their application should be accepted or not.

## Results

#### Data Preprocessing
-The target for this model is the designation provided in the data for successful, the "IS_SUCCESSFUL" column, which indicates whether the money given was used effectively by the recipient
-There are many features for the model, all characteristics of the funding recipient as well as some information about the funding itself. These features are the type of application, the sector of industry, the government organization classification, the use case for the funding, the organization type, whether the organization is active or not, their income classification, special considerations, and lastly the amount of funding requested.
-The "EIN" and "NAME" columns are just identification data and have been removed from the data prior to analysis.

#### Compiling, Training, and Evaluating the Model

-We used the Relu activation function as it is the most commonly used function for classification models. After bucketing and running OneHot encoding on the features we were left with 43 input features, so the first hidden layer had 80 neurons, which is near to the recommended 2 to 3 times the amount of features that is generally recommended. We also used a second layer with 40 neurons to try and accoutn for the complexity of the data.
-We fell just short of the target performance, with an overall model accuracy of about 73%.
--We tried additional models and all of them acheived very similar results, within a percentage point or two in accuracy. We tried adding another hiden layer, adding more neurons to the existing model, and changiong the activation function on the hidden layers to sigmoid, but none saw a significant increase, or decrease, in the performance of the model.

#### Results
-The model fell short of desired results and the strikingly similar results of the variations on the model suggest a different approach might be required. I would like to run the Random Forest Classifier on this data, as it is capable of taking in the large number of features and not applying undue weight. It is generally considered a strong model for classification purposes and would be a good alternative to the model we have already developed.
