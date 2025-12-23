# Liver Fibrosis Prediction – Machine Learning Project

## Project Overview

This project aims to predict the severity of liver fibrosis in patients infected with the Hepatitis C Virus using machine learning methods.  
The objective is to study whether clinical and biological data can help distinguish between early and advanced stages of fibrosis and support clinical decision-making.

This work follows an exploratory and data-driven approach.

## Dataset

The dataset contains routinely collected clinical and biological variables.  
Initially, fibrosis severity was defined using four classes. However, due to poor performance with this formulation, the problem was later reformulated as a binary classification task:

- **Class 0**: Early fibrosis (stages 1 and 2)  
- **Class 1**: Advanced fibrosis (stages 3 and 4)

This binary formulation has stronger clinical meaning and led to better model performance.

## Methodology

The project includes the following steps:
- Data preprocessing (scaling, imputation, encoding)
- Baseline models (Logistic regression, Decision tree, SVM, random forest)
- Dimensionality reduction (PCA)
- Feature selection methods:
  - SelectKBest
  - RFE
  - Mutual information
  - Chi²
  - SelectFromModel
- Hyperparameter tuning using GridSearchCV
- Advanced models (XGBoost, LightGBM)
- Ensemble methods (Bagging, Voting Classifier)
- Neural network for binary classification
- Model evaluation using accuracy, macro F1-score, recall, and confusion matrices

## Results

- The initial **4-class classification** produced very low performance.
- Reformulating the task as a **binary classification** significantly improved results.
- The **best results** were obtained using **SelectKBest + PCA**, with accuracy and macro F1-score around **50–52%**.
- Advanced models and ensemble methods improved stability but not performance significantly.
- The neural network showed potential but remained unstable due to dataset size and feature correlations.
- So, the performance is still limited for a clinical use.

## Limitations

- Small dataset size
- Complex and subtle relationships between biomarkers and fibrosis stages

## Future work

- Use larger or external datasets
- Apply stronger cross-validation strategies
- Explore more advanced deep learning strategies

## Conclusion

This project shows that machine learning can identify relevant patterns in clinical data, but reliable clinical prediction requires more data and careful evaluation.  
