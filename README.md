# 📊 Customer Churn Prediction using Machine Learning

## 🔍 Overview
This project focuses on predicting customer churn in a telecommunications company using machine learning techniques. Customer churn refers to the loss of customers over time, and accurately predicting churn helps businesses take proactive retention measures.

The dataset consists of **7,043 customers** with demographic, behavioral, and service-related features. The goal is to classify customers into:
- Stayed
- Churned
- Joined

## 📁 Dataset Description
The dataset includes features such as:
- Demographics (Age, Gender, Marital Status)
- Subscription details (Internet Service, Contract Type)
- Usage patterns (Monthly Charges, Data Usage)
- Customer lifecycle (Tenure, Referrals)
- Target variable: **Customer Status**

## ⚙️ Project Workflow

### 1. Data Preprocessing
- Removed irrelevant columns (e.g., Customer ID, Zip Code, Latitude/Longitude)
- Handled missing values using interpolation and row filtering
- Encoded categorical variables:
  - Label Encoding for binary features
  - One-Hot Encoding for multi-category features
- Feature scaling using **MinMaxScaler**

### 2. Exploratory Data Analysis (EDA)
Key analyses performed:
- Distribution analysis of numerical features
- Churn vs Non-Churn comparisons
- Correlation heatmap to identify relationships between variables
- Outlier detection using boxplots
- Customer segmentation based on:
  - Payment Method
  - Offers
  - Demographics

📌 insights:
- Customers with shorter tenure show higher churn tendency
- Contract type plays a significant role in retention
- Monthly charges and total charges correlate strongly with churn behavior

### 3. Feature Engineering
- Converted categorical variables into numerical format
- Created a high-dimensional feature space (~1100+ features after encoding)
- Normalized numerical features for model compatibility

### 4. Model Building
Multiple machine learning models were tested:

| Model                  | Description |
|----------------------|------------|
| Logistic Regression  | Baseline linear model |
| Random Forest        | Ensemble-based model |
| Decision Tree        | Tree-based classifier |
| Gaussian Naive Bayes | Probabilistic model |
| XGBoost              | Gradient boosting model |

### 5. Model Selection
Using **GridSearchCV with cross-validation**, the best-performing model was:

✅ **XGBoost Classifier**

- Best CV Score: **~0.827**
- Test Accuracy: **80.86%**

### 6. Evaluation
- Accuracy Score: **80.86%**
- Confusion Matrix used to evaluate prediction performance
- Model effectively distinguishes between churned and retained customers

## 📊 Results & Insights
- XGBoost outperformed all other models
- Strong predictors of churn include:
  - Contract type
  - Monthly charges
  - Tenure
- High-dimensional encoding improved model performance but increased complexity

## 🛠️ Technologies Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Scikit-learn
- XGBoost

👩‍💻 Author
Meher Durdana Khan
