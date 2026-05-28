# AUSWeather
Rainfall Prediction Classifier
Project Overview
Predicting the weather is notoriously difficult due to micro-climatic variations across different geographic regions. This project solves the problem of localizing weather predictions by focusing on a specific 18 km geographic cluster in the Melbourne area (including Melbourne, Melbourne Airport, and Watsonia).
Furthermore, this code addresses a critical data leakage problem common in weather forecasting. Instead of using today's full-day metrics to predict tomorrow's rain, the approach is shifted to a highly practical application: predicting today's rainfall using historical weather data collected up to and including yesterday. This creates a realistic classification model that could help a user decide on their daily commute (e.g., whether to bike to work).
Key Learnings
Through this project, several advanced data science concepts and Python libraries were implemented and mastered:
Scikit-learn Pipelines: Built clean, robust end-to-end workflows by combining data preprocessing steps directly with machine learning estimators (Pipeline).
Advanced Feature Engineering: Cleaned high-cardinality data and extracted temporal patterns by mapping specific calendar months into a brand new Season feature (Summer, Autumn, Winter, Spring).
Automated Preprocessing (ColumnTransformer): Systematized the handling of mixed data types by automatically scaling numeric features via StandardScaler and one-hot encoding categorical variables via OneHotEncoder.
Hyperparameter Tuning: Utilized GridSearchCV combined with StratifiedKFold cross-validation to combat imbalanced target data and optimize model performance.
Model Evaluation & Interpretability: Evaluated performance differences between a tree-based ensemble (Random Forest Classifier) and a linear model (Logistic Regression) using confusion matrices, classification reports, and feature importance mappings.
Dataset
The dataset consists of daily meteorological observations from 2008 to 2017.
Original Source: Australian Government's Bureau of Meteorology (BOM Climate Data).
Curated Source: Downloaded via Kaggle from the weatherAUS.csv dataset (originally packaged for the R rattle software).
The raw dataset tracks 23 distinct fields, including minimum/maximum temperatures, rainfall, evaporation, sunshine hours, wind speeds/directions, humidity, atmospheric pressure, and cloud fractions.
