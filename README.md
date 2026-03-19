# 🚴 Bike Rental Demand Prediction

## 1. 📌 Problem Statement

Rental bikes have become an essential part of urban transportation systems. Ensuring bike availability at the right time is critical to improving user experience and reducing waiting time.

The main challenge is to accurately predict hourly bike rental demand so that supply can be efficiently managed.

---

## 2. 📂 Dataset Description

The dataset contains hourly bike rental counts along with weather and time-based features.

### 🔑 Key Features:

- **Date** → Year-Month-Day  
- **Rented_Bike_Count** → Target variable (number of bikes rented per hour)  
- **Hour** → Hour of the day  
- **Temperature** → °C  
- **Humidity** → %  
- **Wind Speed** → m/s  
- **Visibility** → meters  
- **Dew Point Temperature** → °C  
- **Solar Radiation** → MJ/m²  
- **Rainfall** → mm  
- **Snowfall** → cm  
- **Seasons** → Winter, Spring, Summer, Autumn  
- **Holiday** → Holiday / No Holiday  
- **Functioning Day** → Functional / Non-functional day  

---

## 3. 🎯 Objective

The main objectives of this project are:

- Predict the number of bikes rented per hour  
- Analyze the impact of weather and time-based features  
- Build and compare multiple machine learning models  
- Improve performance using Boosting algorithms and Hyperparameter Tuning  

---

## 4. 🛠 Proposed Solution

### 4(a). ⚙️ Methodology

The project follows a complete Machine Learning Pipeline:

#### 🔹 Data Preprocessing
- Handled missing values  
- Extracted features from date (year, month, day)  
- Removed multicollinearity using VIF  
- Treated outliers using capping  
- Separated numerical and categorical features  

#### 🔹 Feature Engineering
- Applied:
  - Label Encoding  
  - One-Hot Encoding  
- Performed feature selection based on:
  - Correlation  
  - Feature importance  

#### 🔹 Model Training

**📌 Traditional Models:**
- Linear Regression  
- Ridge Regression  
- Lasso Regression  
- K-Nearest Neighbors  
- Random Forest  

**🚀 Boosting Models:**
- Gradient Boosting Regressor  
- XGBoost Regressor  
- LightGBM Regressor  

#### 🔹 Hyperparameter Tuning
- Applied GridSearchCV on XGBoost  
- Tuned parameters:
  - `learning_rate`  
  - `max_depth`  
  - `n_estimators`  

---

### 4(b). 📊 Result / Evaluation Metrics

Models were evaluated using:

- MSE (Mean Squared Error)  
- RMSE (Root Mean Squared Error)  
- R² Score  
- Adjusted R² Score  

---

### 📸 Final Model Performance


![Model Performance](./assets/model_results.png)

---

### 🔥 Key Insights

- Boosting models significantly outperform traditional models  
- LightGBM achieved the best performance  
- Hyperparameter tuning improved XGBoost results  
- Feature engineering and outlier handling played a crucial role  

---

## 5. ✅ Conclusion

- Weather and time-based features strongly influence bike demand  
- Boosting algorithms (LightGBM, XGBoost) provide high accuracy  
- Traditional models perform poorly due to non-linearity  
- Proper preprocessing and feature engineering significantly improve performance  

👉 The final model can be used for:
- Real-time bike demand prediction  
- Efficient resource allocation  
- Reducing customer waiting time  