# Churn Prediction for E-commerce Platform
This project predicts user churn based on their activities on an e-commerce platform and provides actionable insights to improve user retention. Below are the details about the project structure and implementation.
________________________________________
Project Overview
The goal of this project is to:
1.	Predict which users are likely to churn.
2.	Provide insights into user behavior to understand the reasons behind churn.
Dataset
•	File Name: events.csv
•	Columns:
o	event_time: Timestamp of the event.
o	event_type: Type of activity (view, cart, or purchase).
o	product_id: Identifier for the product.
o	category_id: Identifier for the product category.
o	category_code: Human-readable category name.
o	brand: Brand of the product.
o	price: Price of the product.
o	user_id: Identifier for the user.
o	user_session: Identifier for the session.
________________________________________
Steps in the Notebook
1. Data Loading and Preprocessing
•	Load the dataset and parse the event timestamps.
•	Handle missing or inconsistent data.
•	Perform feature transformations (e.g., extracting session durations).
2. Exploratory Data Analysis (EDA)
•	Visualize activity distributions over time.
•	Analyze user-level metrics such as session counts and total purchases.
•	Identify trends and anomalies in user behavior.
3. Defining Churn
•	Churn is defined as users who have not made a purchase or visited the platform in the last 30 days.
•	New users with less than 30 days of data are excluded from the analysis.
4. Feature Engineering
•	Behavioral Features: View-to-cart and cart-to-purchase ratios.
•	RFM Metrics: Recency, frequency, and monetary value of user activity.
•	Session Metrics: Average session duration, bounce rates, and total sessions.
•	Category Preferences: Most viewed or purchased categories and brands.
•	Encode categorical features and scale numerical data.
5. Modeling and Evaluation
•	Models: Logistic Regression, Random Forest, and XGBoost.
•	Metrics: Accuracy, Precision, Recall, F1-score, and AUC-ROC.
•	Hyperparameter tuning is performed using GridSearchCV.
6. Interpretability and Insights
•	Use SHAP values to identify influential features.
•	High recency scores and low cart-to-purchase ratios are strong predictors of churn.
________________________________________
Key Results
1.	Model Performance: XGBoost achieved the highest AUC-ROC, indicating robust performance on imbalanced data.
2.	Actionable Insights:
o	Users with long inactivity or low conversion rates are at higher churn risk.
o	Categories with high churn rates may need product or pricing improvements.
3.	Business Recommendations:
o	Offer retention campaigns for at-risk users (e.g., discounts or personalized offers).
o	Focus on improving high-churn product categories.
________________________________________
How to Run the Code
1.	Place the events.csv file in the working directory.
2.	Install required libraries (e.g., pandas, matplotlib, scikit-learn, XGBoost).
3.	Run the notebook step-by-step to:
o	Load and preprocess data.
o	Perform EDA and feature engineering.
o	Train and evaluate models.
________________________________________

