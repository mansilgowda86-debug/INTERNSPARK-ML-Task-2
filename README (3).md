# 🏠 House Price Prediction using Machine Learning

## 📌 Project Overview

This project builds a Machine Learning regression model to predict house prices based on various property features. The workflow includes data preprocessing, feature engineering, exploratory data analysis (EDA), model training, evaluation, and prediction on new data.

The objective is to compare multiple regression algorithms and identify the best-performing model for accurate house price prediction.

---

## 📂 Dataset

**Dataset Source:**
https://www.kaggle.com/datasets/bhanupratapbiswas/house-price-prediction

The dataset contains information about houses such as:

- Area
- Number of Bedrooms
- Number of Bathrooms
- Stories
- Parking
- Main Road Access
- Guest Room
- Basement
- Air Conditioning
- Furnishing Status
- Preferred Area
- House Price (Target)

---

## 🎯 Project Goals

- Perform Exploratory Data Analysis (EDA)
- Handle missing values
- Apply feature engineering and transformations
- Encode categorical features
- Scale numerical features
- Train multiple regression models
- Compare model performance
- Perform residual analysis
- Save the best model
- Demonstrate predictions on unseen data

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

---

## 📊 Exploratory Data Analysis

The notebook includes:

- Dataset overview
- Missing value analysis
- Summary statistics
- Correlation heatmap
- Target variable distribution
- Pairwise feature visualization
- Feature relationship analysis

---

## ⚙️ Data Preprocessing

The following preprocessing steps are performed:

### Missing Value Handling

- Numerical columns → Median Imputation
- Categorical columns → Most Frequent Imputation

### Feature Transformation

- Log Transformation of target variable (`price`)
- One-Hot Encoding for categorical features
- Standard Scaling for numerical features

---

## 🤖 Machine Learning Models

The following regression algorithms are trained and compared:

1. Linear Regression
2. Random Forest Regressor
3. Gradient Boosting Regressor

---

## 📈 Evaluation Metrics

The models are evaluated using:

- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score

Additional evaluation includes:

- Residual Plot
- Actual vs Predicted Plot
- Feature Importance Visualization

---

## 📁 Project Structure

```
House-Price-Prediction/
│
├── Housing.csv
├── House_Price_Prediction.ipynb
├── house_price_model.pkl
├── processed_house_price.csv
├── README.md
└── requirements.txt
```

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/House-Price-Prediction.git
```

### 2. Navigate to the project directory

```bash
cd House-Price-Prediction
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```
House_Price_Prediction.ipynb
```

Run all cells.

---

## 💾 Saved Model

The best-performing model is saved as:

```
house_price_model.pkl
```

using the Joblib library.

---

## 🔮 Example Prediction

```python
import pandas as pd
import joblib
import numpy as np

model = joblib.load("house_price_model.pkl")

sample = pd.DataFrame({
    "area":[7420],
    "bedrooms":[4],
    "bathrooms":[2],
    "stories":[3],
    "mainroad":["yes"],
    "guestroom":["no"],
    "basement":["no"],
    "hotwaterheating":["no"],
    "airconditioning":["yes"],
    "parking":[2],
    "prefarea":["yes"],
    "furnishingstatus":["furnished"]
})

prediction = model.predict(sample)

print("Predicted House Price:", np.expm1(prediction[0]))
```

---

## 📊 Results

The trained models are compared using:

| Model | RMSE | MAE | R² Score |
|--------|------|-----|----------|
| Linear Regression | Calculated in Notebook | Calculated in Notebook | Calculated in Notebook |
| Random Forest | Calculated in Notebook | Calculated in Notebook | Calculated in Notebook |
| Gradient Boosting | Calculated in Notebook | Calculated in Notebook | Calculated in Notebook |

The model with the lowest RMSE and MAE and the highest R² score is selected as the best-performing model.

---

## 🚀 Future Improvements

- Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
- Cross-validation for robust performance evaluation
- Feature selection techniques
- XGBoost, LightGBM, and CatBoost implementation
- SHAP analysis for model explainability
- Deploy the model using Flask, FastAPI, or Streamlit

---
