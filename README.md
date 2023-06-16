# Bike Share Demand Prediction
*Predicting demand with the Capital Bike Share dataset from [Kaggle](https://www.kaggle.com/competitions/bike-sharing-demand/overview)*

The objective was to predict demand for shared bikes in Washington, D.C., given 2 years of data. The dataset was artificially split so that the selection available to create the model consists of hourly data from the 1st to 19th days of the month, with the remaining data (from the 20th until the end of the month for all months) used for testing (which is done automatically by Kaggle upon upload).

I've only included the models with the best result obtained via Kaggle, one linear regression in **linear_regression.ipynb** (RMSLE: 0.9677) and one random forest in **random_forest.ipynb** (RMSLE: 0.54805). For context, the best score publicly available on Kaggle was 0.33756.

This project took me around 2 person days to complete to its current status.

# Process
This process was the same for both methods (see **linear_regression.ipynb** and **random_forest.ipynb**)
1. Import relevant libraries and explore the data (see **eda.ipynb**); note that, despite the naming structure, "train.csv" is used for training and testing the model while "test.csv" is for applying the trained and tested model
2. Split
3. Feature engineering with sklearn pipeline and column transformer
4. Fit and test model, cross-validation, calculate split "train" RMSLE
5. Export and upload to Kaggle for "test" RMSLE

# Next
If I dedicated more time to this project, I would further tweak my variables in pursuit of a better score and would implement a Voting Classifier.
As I do however see the dataset as potentially inherently skewed because of the way it's been split (train.csv only includes data from the 1st to 19th days of the month, the remaining data are found in test.csv), it's unlikely I'll come back to this.