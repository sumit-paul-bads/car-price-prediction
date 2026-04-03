# 🚗 Car Price Prediction using Machine Learning

## 📌 Project Overview
This project builds a machine learning model to predict the price of used cars based on various features such as company, fuel type, kilometers driven, and car age.

The goal was to develop a complete end-to-end ML pipeline — from data cleaning and exploratory analysis to model training, evaluation, and deployment readiness.

---

## 🎯 Objective
- Predict used car prices accurately
- Understand key factors affecting car valuation
- Build a scalable ML pipeline for real-world usage

---

## 📂 Dataset Features
The dataset includes the following key features:

- `company` → Car manufacturer (e.g., Hyundai, Maruti, Ford)
- `model` → Extracted car model name
- `fuel_type` → Petrol / Diesel
- `kms_driven` → Distance traveled
- `year` → Manufacturing year
- `price` → Target variable

---

## 🧹 Data Cleaning & Preprocessing
- Handled missing values
- Cleaned and standardized car names
- Extracted `model` from raw text
- Created `car_age` feature from year
- Removed irrelevant columns
- Ensured consistent data types

---

## 📊 Exploratory Data Analysis (EDA)
- Identified skewed price distribution
- Observed:
  - Price decreases as kilometers driven increases
  - Older cars generally cost less
- Detected outliers in high-price segment
- Used visualizations:
  - Histograms
  - Boxplots
  - Scatter plots
  - Correlation heatmap

---

## 🔄 Feature Engineering
- Applied log transformation:
  - `price → log_price`
  - `kms_driven → log_kms_driven`
- Helped normalize data and reduce outliers
- Tested interaction feature (`age × kms`)
  - No improvement → removed

---

## ⚙️ Model Pipeline
Used `scikit-learn` pipeline with:

### Preprocessing:
- OneHotEncoding for categorical variables
- StandardScaler for numerical features

### Models Evaluated:
- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest
- XGBoost

---

## 🔁 Hyperparameter Tuning
- Used **GridSearchCV**
- Applied **cross-validation**
- Selected model based on **R² score**

---

## 🏆 Best Model
**Ridge Regression (alpha = 1)**

Reason:
- Best balance between bias and variance
- Stable performance across folds
- Better generalization than tree-based models

---

## 📈 Model Performance

### Test Results:
- **R² Score:** ~0.776  
- **RMSE (log scale):** ~0.388  
- **RMSE (actual price):** ~₹2.7 Lakhs  

---

## 📉 Model Insights

### ✅ Strengths:
- Accurate for mid-range vehicles
- Captures general pricing trends well

### ⚠️ Limitations:
- Less accurate for high-value cars
- Data imbalance affects predictions
- Residuals show heteroscedasticity

---

## 📊 Visualizations
- Price distribution (before & after log transform)
- Scatter plots (Price vs KMs, Log transformations)
- Correlation heatmap
- Actual vs Predicted plot
- Residual analysis

---

## 💾 Outputs
- 📄 `car_price_predictions.csv` → Predictions
- 🤖 `car_price_model.pkl` → Trained model (pipeline)

---

## 🎥 Project Demo

https://drive.google.com/file/d/1j6nce3bGgyB34tGBAhYiI7-0o-9-rwcS/view?usp=sharing

---

## 🚀 Future Improvements
- Add more features (transmission, ownership, location)
- Handle imbalance in high-price cars
- Use advanced boosting models (LightGBM, tuned XGBoost)
- Deploy using Streamlit

---

## 🛠️ Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- Joblib

---

## 📌 Conclusion
This project demonstrates a complete machine learning workflow — from raw data to a deployable model. It highlights the importance of preprocessing, feature engineering, and model evaluation in building reliable predictive systems.

---

## 🙌 Author
**Sumit Paul**
