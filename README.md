# 🛍️ Local Artisan Product Price Prediction

This project aims to build a regression model to predict the **lowest price** (`Low_Cap_Price`) at which local artisan products can be sold, ensuring that promotional discounts do not negatively impact local producers. The model is built using machine learning techniques on structured market data.

---

## 📁 Dataset Description

The dataset consists of information on product characteristics, market categories, and pricing:

| Column              | Description                                               |
|---------------------|-----------------------------------------------------------|
| `Item_Id`           | Unique product identifier                                 |
| `Date`              | Date of product listing or price capture                  |
| `State_of_Country`  | State number where the market is located                  |
| `Market_Category`   | Category of the market                                    |
| `Product_Category`  | Category of the product                                   |
| `Grade`             | Product quality grade                                     |
| `Demand`            | Demand of the product in the market                       |
| `Low_Cap_Price`     | 🔥 **Target**: Lowest allowable selling price             |
| `High_Cap_Price`    | Maximum price in the current market                       |

---

## 📂 Files in This Repository

| File Name             | Description                                               |
|------------------------|-----------------------------------------------------------|
| `Train.csv`            | Training dataset with features and target                 |
| `Test.csv`             | Test dataset for prediction                               |
| `sample_submission.csv`| Sample format for submission                              |
| `price_prediction.ipynb`| Jupyter notebook with full workflow (EDA → modeling)     |
| `submission.csv`       | Final predicted `Low_Cap_Price` values on test set        |
| `README.md`            | This file ✍️                                               |

---

## 🧠 Project Workflow

### Step 1: Data Loading & Cleaning
- Load training and test sets
- Handle missing values (if any)
- Convert `Date` to datetime format

### Step 2: Exploratory Data Analysis (EDA)
- Analyze target distribution
- Visualize relationships between features and `Low_Cap_Price`
- Explore categorical feature effects using boxplots

### Step 3: Feature Engineering
- Extract features like `Year`, `Month` from `Date`
- One-hot encode categorical variables
- Align train/test feature columns for consistency

### Step 4: Model Building & Evaluation
- Use models like:
  - Random Forest Regressor 🌳
  - Linear Regresson ⚡
- Evaluate using RMSE (Root Mean Squared Error)

### Step 5: Prediction & Submission
- Predict `Low_Cap_Price` on test data
- Export predictions to CSV in required format

---

## 📈 Model Performance

| Model             | RMSE on Validation |
|-------------------|--------------------|
| Random Forest      | *0.86*              |
| Linear Regression           | *0.777*              |

---

## 📌 Future Improvements

- Use more advanced hyperparameter tuning (Optuna / GridSearch)
- Try feature selection using SHAP or permutation importance
- Try ensemble blending or stacking for better performance

---

## 🤝 Acknowledgements

- Inspired by real-world e-commerce challenges supporting local artisans.
- Provided dataset is synthetic but mimics realistic pricing conditions.


