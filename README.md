# Credit Card Default Prediction

## Project Overview
This project focuses on predicting credit card defaults using binary classification techniques. The dataset, sourced from [Kaggle](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset), provides demographic, financial, and behavioral information on credit card clients.

## Dataset
The dataset is sourced from the kaggle and is accessible via the following [link]([https://archive.ics.uci.edu/dataset/109/wine](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset)).

## Key Features
- **Dataset Size**: 30,000 samples and 24 features.
- **Target Variable**: `default.payment.next.month` (1 = Default, 0 = No Default).
- **Highlights**:
  - Exploratory Data Analysis (EDA).
  - Preprocessing and Feature Engineering.
  - Model Training and Evaluation (LGBM, CatBoost, Logistic Regression).
  - Dimensionality Reduction using PCA.
  - Handling Data Imbalance with SMOTETomek.

## Project Structure
```
├── data/
│   ├── UCI_Credit_Card.csv # Original dataset
│   ├── df_prep.csv # Prepped dataset for further analysis
├── notebooks/
│ ├── Credit_Card_Default.ipynb
│ └── Credit_Card_Default.py
├── models/
│   ├── best_LGBM.sav # Trained LGBM model
│   ├── best_CatBoost.sav # Trained CatBoost model
│   └── best_logr.sav # Trained Logistic Regression model
└──  README.md
```

## Key Steps

### 1. **Data Preprocessing**
- Handled missing values and cleaned the dataset.
- Standardized numerical features using `StandardScaler` for better model performance.
- Used **SMOTE** to balance the dataset by oversampling the minority class.

### 2. **Feature Engineering**
- Applied **PCA** to reduce dimensionality and assess the impact on model performance.
- Retained key features while exploring the effect of feature reduction.

### 3. **Modeling**
- Trained and evaluated multiple models, including:
  - Logistic Regression
  - Random Forest
  - LightGBM (LGBM)
  - CatBoost
- Hyperparameter tuning was performed using **GridSearchCV** for the best-performing models.

### 4. **Evaluation**
- Evaluated models using cross-validation and metrics:
  - **Accuracy**: Overall correctness of predictions.
  - **Precision**: Proportion of true positives among predicted positives.
  - **Recall**: Ability to detect the positive class (critical in imbalanced datasets).
  - **F1 Score**: Harmonic mean of precision and recall.
  - **ROC-AUC**: Area under the ROC curve to assess model discrimination ability.

### 5. **Final Model**
- The final model was selected based on performance across metrics and practical considerations, such as computation time.
- The selected model's performance was checked on standard, SMOTE and PCA dataset to confirm whether the performed operations had a positive effect.
- The selected model was evaluated on the test set for unbiased performance estimation.


## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Zanyata/Default-of-Credit-Card.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Default-of-Credit-Card
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
---

For further improvements or questions, feel free to create an issue or contact the repository owner.

