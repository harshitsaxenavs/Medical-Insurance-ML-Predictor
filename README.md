# 🏥 Medical Insurance Cost Prediction

## 📌 Project Overview
This project predicts medical insurance charges using a supervised machine learning model trained on demographic and health-related data such as age, BMI, smoking status, gender, and region.

It includes a complete end-to-end Data Science workflow:
EDA → Feature Engineering → Statistical Feature Selection → Preprocessing → Model Training → Evaluation.

## 📂 Dataset Overview
The dataset contains 1,338 entries with the following features:

| Column   | Description                                      | Type        |
|----------|--------------------------------------------------|-------------|
| age      | Age of the primary beneficiary                   | Numerical   |
| sex      | Gender of the individual                         | Categorical |
| bmi      | Body mass index                                  | Numerical   |
| children | Number of dependents                             | Numerical   |
| smoker   | Smoking status (yes/no)                          | Categorical |
| region   | Residential region in the US                     | Categorical |
| charges  | Individual medical insurance cost                | Target      |

## 🛠️ Tech Stack
- Python
- Pandas, NumPy – Data handling
- Matplotlib, Seaborn – Visualizations
- Scikit-Learn – Model building & preprocessing
- SciPy – Statistical tests

## 📊 Key Workflow Steps

### 1. Data Cleaning & EDA
- Identified duplicates and missing values
- Distribution analysis of Age, BMI, Charges
- Correlation heatmap

Key Insight: Smoking status had the strongest correlation with charges (0.78).

### 2. Feature Engineering
- Created BMI Categories (Underweight, Normal, Overweight, Obese)
- Label Encoding for binary variables (sex, smoker)
- One-Hot Encoding for nominal variables (region, bmi_categories)

### 3. Feature Selection
- Pearson Correlation for numeric features
- Chi-Square Test for categorical features

Removed: region_northwest, region_southwest, bmi_categories_Normal.

### 4. Data Preprocessing
- Scaled numerical features (age, bmi, children) using StandardScaler.

### 5. Model Building & Evaluation

| Model              | MSE         | R² Score | Adjusted R² |
|--------------------|-------------|----------|--------------|
| Linear Regression  | 36,003,101  | 0.804    | 0.798        |
| Random Forest      | 24,718,888  | 0.865    | 0.861        |

Conclusion: Random Forest performed best.

## 🚀 How to Run

```bash
git clone https://github.com/harshitsaxenavs/Medical-Insurance-ML-Predictor.git
cd Medical-Insurance-ML-Predictor
pip install pandas numpy seaborn matplotlib scikit-learn scipy
jupyter notebook project1.ipynb
```

## 📈 Future Improvements
- GridSearchCV tuning
- Try XGBoost / Gradient Boosting
- Deploy as Streamlit / Flask app

## 👨‍💻 Author
Harshit Saxena  
B.Tech CSE • Maharaja Surajmal Institute of Technology, Delhi  

📧 harshitsaxenavs@gmail.com  
GitHub: https://github.com/harshitsaxenavs  

## ⚠️ License
This project is not open-source. All rights reserved.
