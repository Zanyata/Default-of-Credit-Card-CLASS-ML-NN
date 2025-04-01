# Credit Card Default Prediction


## Overview
This project focuses on predicting credit card defaults using binary classification techniques. The dataset, sourced from Kaggle, provides demographic, financial, and behavioral information on credit card clients.
Multiple models were benchmarked and tuned, including preprocessing strategies, feature selection (SHAP, Boruta), and dimensionality reduction (PCA, VIF). The project culminates in selecting the best model pipeline and evaluating performance across multiple metrics.


## Table of Contents
- [Dataset](#dataset)
- [Data Preprocessing](#Data-Preprocessing)
- [Models Evaluated](#Models-Evaluated)
- [Evaluation](#Evaluation)
- [Models Evaluated](#Models-Evaluated)
- [Best Performing Model](#Best-Performing-Model)
- [Project Organization](#Project-Organization)
- [Installation & Usage](#Installation-&-Usage)


## Dataset
The dataset is sourced from the kaggle and is accessible via the following [link](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset).
- **Dataset Size**: 30,000 samples and 23 features.
- **Demographic data** (e.g., age, sex, education, marriage)
- **Financial attributes** (credit limit, bill statements, payments)
- **Target Variable**: `default.payment.next.month` (1 = Default, 0 = No Default).


## **Data Preprocessing**

**Feature Engineering:**
- Handled missing values and cleaned the dataset.
- Standardized numerical features using `StandardScaler` for better model performance.

**Feature Selection:**
- Multicollinearity check
- SHAP and BorutaPy
- Applied **PCA** to reduce dimensionality and assess the impact on model performance.

**Data Splitting:**
- Training, validation, and test sets created using stratified sampling.


## **Evaluation**
- Evaluated models using cross-validation and metrics:
  - **Accuracy**: Overall correctness of predictions - one of the most informative metrics
  - **Precision**: Proportion of true positives among predicted positives.
  - **Recall**: Ability to detect the positive class (critical in imbalanced datasets).
  - **F1 Score**: Harmonic mean of precision and recall - one of the most informative metrics
  - **ROC-AUC**: Area under the ROC curve to assess model discrimination ability - one of the most informative metrics

## Models Evaluated
1. **Classification** - LightGBM, CatBoostClassifier
2. **Neural Network**

## Best Performing Model
- **Neural Network** Best Test F1, best AUC, best accuracy



## Project Organization
```
├── LICENSE                               <- Open-source license
├── README.md                             <- Project documentation
├── data/
│   ├── raw                               <- Raw Data
│   └── processed                         <- The final, canonical data sets for modeling
│
├── models                                <- Trained models, model predictions, or model summaries
│
├── notebooks                             <- Jupyter notebooks
│   └── 1.0-Default-of-Credit-Card.ipynb  <- Code with data preprocessing and models
│
├── reports                               <- Generated analysis
│   └── figures                           <- The most important generated graphics and figures
│
└── requirements.txt                      <- Python dependencies
```


## Installation & Usage
1. Clone the repository:
```bash
git clone https://github.com/Zanyata/Default-of-Credit-Card_CLASS-ML.git
```
```bash
cd Default-of-Credit-Card
```
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Run Jupyter Notebook:
```bash
jupyter notebook
```
--------