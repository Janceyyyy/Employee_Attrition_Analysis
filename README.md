# Employee Attrition Analysis

## Overview
This project aims to predict employee attrition using a dataset maintained by IBM, consisting of 1,470 data points and 32 features. 

## Dataset
The dataset features employee personal information, company-specific information, and work-life balance conditions. After preprocessing, the dataset included 46 features.

## Technology and Models Used
- **Python**: Main programming language.
- **Pandas & NumPy**: Data manipulation and numerical operations.
- **Scikit-learn**: Data preprocessing, model training, and evaluation.
  - **Used models:** Logistic Regression with L2 regularization (Ridge), RandomForestClassifier, XGBoost, K-Nearest Neighbors (KNN), and Support Vector Machine (SVM).
- **XGBoost**: Achieved the highest F1-score, used for final model training.
- **Matplotlib & Seaborn**: Data visualization.

## Methodology
1. **Exploratory Data Analysis (EDA)**: Distribution checks, zero-variance, missing and duplicate value checks, and bivariate analysis.
2. **Data Preprocessing**: Utilized StandardScaler, OneHotEncoder, and OrdinalEncoder for feature encoding. Performed stratified K-fold splits due to imbalanced data.
3. **Model Training and Hyperparameter Tuning**: Employed GridSearchCV for optimal parameter discovery across multiple models, with a focus on maximizing the F1-score due to data imbalance.
4. **Feature Importance Analysis**: Utilized permutation importance, built-in feature importance in XGBoost, and SHAP values to identify key predictors of attrition.

## Results
- The XGBoost model outperformed other models, achieving an F1-score significantly above the baseline.
- Key predictors identified include 'OverTime', 'MonthlyIncome', and 'EnvironmentSatisfaction'.

## Future Work
Suggestions include updating the dataset to reflect current work trends like remote work, exploring SMOTE for addressing data imbalance, and incorporating additional models such as LightGBM for improved predictions.

## References
- IBM HR Analytics Employee Attrition & Performance Dataset from Kaggle.
- Relevant publications and competitions on Kaggle for comparison and model validation strategies.


## Project Structure

This repository is organized as follows:
.
├── `data/`
│   └── This directory contains the dataset used for analysis.
├── `figures/`
│   └── This directory contains visualizations and graphs generated during the analysis.
├── `results/`
│   ├── `KNN.save` - The saved K-Nearest Neighbors model.
│   ├── `Ridge.save` - The saved Ridge Regression model.
│   ├── `rf2.save` - The saved Random Forest model (second version with different parameters or data).
│   ├── `SVC.save` - The saved Support Vector Classifier model.
│   └── `XGB.save` - The saved XGBoost model.
├── `report/`
│   └── This directory contains the detailed project report in PDF format.
├── `src/`
│   ├── `overview of the features.xlsx` - Overview of the features of data.
│   └── `project.ipynb` - Source code.
├── `.gitignore` - Specifies intentionally untracked files to ignore.
├── `LICENSE` - The license for the project.
└── `README.md` - The README file with information about the project.
