# -Airbnb-Price-Prediction-Data-Analysis-Model-Building
**GitHub Title:**   🏡 **Airbnb Price Prediction Model**    **GitHub Description (Short &amp; Simple):**   This project focuses on predicting **Airbnb listing prices** using **EDA, feature engineering, and machine learning models**. We preprocess data, analyze key features, and implement **regression models** to optimize predictions. 🚀


## Overview
This project involves data preprocessing, exploratory data analysis (EDA), and model training to build a predictive model.

## Dataset Overview
This dataset consists of **74,111 entries** and **11 columns**, primarily related to accommodations, pricing, and booking characteristics.

### **Column Descriptions**
1. **id** *(int64)* - Unique identifier for each listing.  
2. **room_type** *(object)* - Type of room (e.g., Entire home, Private room, Shared room).  
3. **accommodates** *(float64)* - Number of people the listing can accommodate.  
4. **bathrooms** *(float64)* - Number of bathrooms available.  
5. **cancellation_policy** *(object)* - Cancellation flexibility (e.g., Flexible, Moderate, Strict).  
6. **cleaning_fee** *(float64)* - Additional cleaning fee charged.  
7. **instant_bookable** *(object)* - Indicates whether the listing is available for instant booking (Yes/No).  
8. **review_scores_rating** *(float64)* - Average review score rating (may have missing values).  
9. **bedrooms** *(float64)* - Number of bedrooms available.  
10. **beds** *(float64)* - Number of beds provided.  
11. **log_price** *(float64)* - Log-transformed price of the listing (used to normalize pricing).  

### **Key Observations**
- The dataset has **missing values** in **bathrooms, review_scores_rating, beds, and bedrooms** columns.  
- The **log_price column** suggests that price values were log-transformed to handle skewness.  
- **Review scores are missing for many listings (57,389 non-null values)**, which might impact the model's performance.  
- **Instant booking is categorical**, which may require encoding before feeding it into a machine learning model.  

### **Next Steps**
- **Handle missing values** (imputation with mean/median or predictive models).  
- **Encode categorical variables** (e.g., `room_type`, `cancellation_policy`, `instant_bookable`).  
- **Feature scaling** for numerical variables if required.  
- **Explore correlations** between `log_price` and other numerical variables to assess key drivers of pricing.  

## Steps & Analysis

### **1. Data Preprocessing**
- **Handling Missing Values**:
  - Mean imputation
  - Median imputation
  - KNN imputation (using nearest neighbors to fill missing data)
- **Outlier Treatment**:
  - Detected and adjusted extreme values to enhance model performance.

### **2. Exploratory Data Analysis (EDA)**
- **Univariate Analysis**: Examined distributions of individual variables.
- **Bivariate Analysis**: Identified relationships between variables and the target.

### **3. Model Building**
- **Train-Test Split**: Divided the dataset into training and testing sets.
- **Implemented Models**:
  - **Linear Regression**: Basic predictive modeling.
  - **Lasso & Ridge Regression**: Regularization techniques to handle multicollinearity.

## Conclusion & Next Steps
### **Key Takeaways**
- Data imputation techniques improved the dataset’s completeness.
- Regularization methods helped in reducing overfitting.
- Further feature engineering and hyperparameter tuning are required for better accuracy.

### **Action Items**
1. **Optimize Hyperparameters**: Tune model parameters for improved performance.
2. **Feature Engineering**: Create more meaningful features.
3. **Evaluate Additional Models**: Test other machine learning algorithms (e.g., Decision Trees, Random Forest).

---
Developed as part of **Predictive Modeling & Data Science Workflow**.

