# NFL - Predicting a Super Bowl Champion

The purpose of this project is to predict the outcome of the 2020 NFL Super Bowl LV winning team using historical regular season team offense and defense statistics. This is a Binary Classification problem as the result of the Super Bowl has two outcomes, win or lose. The goal is to create a linear regression machine learning model that most accurately predicts the winner. 

# Data Collection & Assembly 

I used several approaches to creating input data and combined the features I found most useful. This data was sourced from http://www.pro-football-reference.com/. 

This is a plain batch dataset complied of 10 regular seasons of Offense, Defense and Super Bowl historical statistics. These csv files were stitched and merged as part of the initial data preprocessing. This dataset contains 11,616 observations and 29 features. 

The dataset had no odd or missing values resulting in zero data being dropped. Were applicable team names were aligned due to franchise rebranding. 

- Oakland Raiders > Las Vegas Raiders
- San Diego Chargers > Los Angeles Chargers
- Washington Redskins > Washington Football Team
- St. Louis Rams > Los Angeles Rams

3 primary files: NFL Historical Statistics – Offense; NFL Historical Statistics – Defense; NFL Historical Statistics – Super Bowl Winners

# Model & Parameter Tuning

For the model, I used Sklearn to create a Logistic Regression. 

To reduce multicollinearity between features, I applied Principal Component Analysis (PCA) (n_component = 3).

To account for data imbalance, I derived a ROC curve to identify the optimal threshold. (Best Threshold = 0.016919; G –Mean = 0.856)

To further tune, I ran a GridSearchCV to get the optimal model parameters. 

# Performance Measure 

Baseline Accuracy: 98%
Model Testing Accuracy: 97% (less than Baseline)

