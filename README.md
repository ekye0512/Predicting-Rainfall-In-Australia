# Predicting-Rainfall-In-Australia

## Introduction
Weather significantly impacts daily life, from commutes to activities. This project focuses on predicting whether it will rain the next day in Australia based on historical weather data. We use a dataset from Kaggle covering 2008-2017, with over 20 variables from multiple Australian cities.

## Data
The dataset includes 23 variables:

Quantitative: Max/Min Temperature, Rainfall, Evaporation, Sunshine, Wind Gust Speed, Wind Speed, Humidity, Pressure, Cloud Cover, Temperature at 9 AM and 3 PM.
Categorical: Date, Location, Wind Gust Direction, Wind Direction at 9 AM and 3 PM.
Binary: RainToday, RainTomorrow (Yes/No).
We removed columns deemed unnecessary (Date, Location, Wind Gust Direction, Wind Direction variables) and handled missing values by removing rows with NA values.

## Exploratory Data Analysis (EDA)
Summary Statistics: Variables like Rainfall and Evaporation showed significant variation and outliers.
Correlation Plot: Revealed intuitive correlations, e.g., temperature variables are highly correlated, and Sunshine is negatively correlated with Cloud Cover.
Histograms: Showed variable distributions and highlighted skewness and outliers in Rainfall and Evaporation.

## Methodology
We split the dataset into training (2008-2013) and test (2014-2017) sets. Models tested:

### LDA & QDA: 
Linear and Quadratic Discriminant Analysis.

### Logistic Regression: 
Used a cutoff of 0.5.

### Lasso & Ridge Regression: 
Applied shrinkage penalties with optimal λ values.

### Random Forest:
An ensemble method combining multiple decision trees.

## Conclusion
Model accuracies were similar across methods:

LDA: 83.7%
QDA: 85.4%
Logistic Regression: 85.5%
Lasso: 85.5%
Ridge: 85.1%
Random Forest: 85.7%
While Random Forest had the highest accuracy, simpler models like Logistic Regression and LDA are computationally less intensive and easier to interpret. Future improvements could include using alternative methods, refining data handling techniques, and exploring different model selection approaches.

This study provides a robust foundation for weather prediction models, with potential for further refinement and application in weather forecasting.
