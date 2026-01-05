# Predicting-Airbnb-Rental-Prices-in-London-
Airbnb Price Prediction using Machine Learning
📌 Project Overview

This project investigates whether machine learning models can accurately predict Airbnb listing prices and identifies the key factors influencing price.
Using Airbnb listing data, the project follows a complete data science pipeline, including:

Exploratory Data Analysis (EDA)

Data cleaning and feature engineering

Model training and evaluation

Hyperparameter tuning

Feature importance analysis

Final conclusions answering the research questions

The project is designed for academic assessment and follows best practices in Python, scikit-learn, and XGBoost.

🎯 Research Questions

Can machine learning models accurately predict Airbnb listing prices?

What are the most important factors influencing Airbnb prices?

📂 Dataset

Source: Airbnb Open Data

File: listings.csv.gz (or listings.csv if uncompressed)

Key target variable: price

⚠️ The dataset is not included in this repository due to size restrictions.
Please download it separately and place it in the project root directory.

🧹 Data Cleaning & Feature Engineering

Key preprocessing steps include:

Removing currency symbols from price and converting it to numeric

Handling missing values using median and mode imputation

Extracting numeric values from bathrooms_text

Filtering extreme outliers (5th–95th percentile)

Grouping neighbourhoods into Top 10 + Other

Scaling numerical features

One-hot encoding categorical variables

📊 Exploratory Data Analysis (EDA)

EDA includes:

Price distribution analysis (full range & trimmed)

Univariate analysis of numerical features

Categorical analysis of room and property types

Correlation heatmaps

Boxplots of price by neighbourhood

Key insights from EDA guided feature selection and outlier handling for modelling.

🤖 Machine Learning Models

The following regression models were implemented:

Model	Purpose
Linear Regression	Baseline model
Random Forest Regressor	Non-linear ensemble model
XGBoost Regressor	Gradient boosting model
🔧 Hyperparameter Tuning

RandomizedSearchCV was used for:

Random Forest

XGBoost

3-fold cross-validation

Performance evaluated on unseen test data

📈 Evaluation Metrics

Models were evaluated using:

R² Score – model accuracy

RMSE – prediction error in GBP (£)

🔍 Feature Importance Analysis

To identify key price drivers:

Linear Regression coefficients

Random Forest feature importance

XGBoost feature importance

Consistent important features across models:

Room type (Entire home/apt)

Location (latitude, longitude, neighbourhood)

Property size (accommodates, bedrooms)

Review quality and volume

🧠 Final Conclusions

✅ Yes, machine learning models can accurately predict Airbnb prices

🏆 Best-performing model: Tuned ensemble model (Random Forest / XGBoost)

📌 Most influential factors: Room type, location, size, and reviews

This project successfully answers both research questions using interpretable and high-performing models.

🛠️ Technologies Used

Python 3

pandas, numpy

matplotlib, seaborn

scikit-learn

XGBoost

▶️ How to Run the Project
# Clone the repository
git clone https://github.com/your-username/airbnb-price-prediction.git

# Install dependencies
pip install -r requirements.txt

# Run the full pipeline
python main.py
