# 🏥 Medical Insurance Cost Prediction

## 📌 Project Overview

This project aims to predict individual medical insurance charges using
demographic and health-related data. By analyzing factors such as age,
BMI, smoking habits, and region, we build machine learning models to
estimate insurance costs accurately.

The project implements a complete data science pipeline, including
Exploratory Data Analysis (EDA), Statistical Feature Selection, Feature
Engineering, and Model Evaluation.

## 📂 Dataset

The dataset contains 1,338 rows and 7 columns:

  -------------------------------------------------------------------------
  Column     Description                                      Type
  ---------- ------------------------------------------------ -------------
  age        Age of the primary beneficiary                   Numerical

  sex        Gender (male/female)                             Categorical

  bmi        Body mass index                                  Numerical

  children   Number of children covered by health insurance   Numerical

  smoker     Smoking status (yes/no)                          Categorical

  region     Residential area in the US (ne, nw, se, sw)      Categorical

  charges    Medical costs billed by health insurance         Target
  -------------------------------------------------------------------------

## 🛠️ Tech Stack

-   Python\
-   Pandas & NumPy (Data Manipulation)\
-   Matplotlib & Seaborn (Visualization)\
-   Scikit-Learn (Machine Learning & Preprocessing)\
-   SciPy (Statistical Testing)

## 📊 Key Workflow Steps

### 1. Data Cleaning & EDA

-   Checked for missing values and duplicates\
-   Visualized distributions of BMI, Age, Charges\
-   Correlation heatmaps

**Insight:** Smoking status showed strongest correlation with charges
(0.78)

### 2. Feature Engineering

-   BMI Categorization\
-   Label Encoding (sex, smoker)\
-   One-Hot Encoding (region, bmi_categories)

### 3. Feature Selection

-   Pearson Correlation (numerical)\
-   Chi-Square (categorical)

Dropped: region_northwest, region_southwest, bmi_categories_Normal

### 4. Data Preprocessing

Applied StandardScaler to numerical features.

### 5. Model Building & Evaluation

  Model               MSE          R²      Adjusted R²
  ------------------- ------------ ------- -------------
  Linear Regression   36,003,101   0.804   0.798
  Random Forest       24,718,888   0.865   0.861

**Conclusion:** Random Forest performed best.

## 🚀 How to Run

``` bash
git clone https://github.com/harshitsaxenavs/Medical-Insurance-ML-Predictor.git
cd Medical-Insurance-ML-Predictor
pip install pandas numpy seaborn matplotlib scikit-learn scipy
jupyter notebook project1.ipynb

```

## 📈 Future Improvements

-   GridSearchCV tuning\
-   XGBoost / Gradient Boosting\
-   Deploy via Streamlit / Flask

## 👨‍💻 Author
- Harshit Saxena
- B.Tech CSE | Maharaja Surajmal Institute of Technology, Delhi

- 📧 harshitsaxenavs@gmail.com
- 🌐 LinkedIn
- 💻 GitHub

## ⚠️ License
This project is not open-source.
All rights are reserved by the author.
Unauthorized copying, modification, or distribution is strictly prohibited.


