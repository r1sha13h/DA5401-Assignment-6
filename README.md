# Assignment-6: Missing Data Imputation and Credit Default Prediction

Name: Rishabh Mishra

Roll: DA25M025

DOS: 17th October, 2025

## Description
This Jupyter notebook analyzes the UCI Credit Card dataset to evaluate the impact of different missing data imputation strategies on credit default prediction. The project compares median imputation, linear regression imputation, decision tree imputation, and listwise deletion methods, assessing their effects on logistic regression model performance.

## Dataset
- **Source**: UCI Credit Card dataset (`UCI_Credit_Card.csv`)
- **Target**: Binary classification - predicting credit card default
- **Features**: Payment history (PAY_X), credit limit (LIMIT_BAL), demographic data, bill amounts, and payment amounts
- **Class Imbalance**: 23,364 non-defaulters vs. 6,636 defaulters

## Contents
### Part A: Data Preprocessing and Imputation
- Exploratory data analysis with correlation and feature importance analysis
- Introduction of missing values (10% of samples) in key features: PAY_0, LIMIT_BAL, PAY_2
- Implementation of four missing data strategies:
  - **dfA**: Median imputation
  - **dfB**: Linear regression imputation
  - **dfC**: Decision tree imputation
  - **dfD**: Listwise deletion
- Distribution visualization using KDE plots

### Part B: Model Training and Performance Assessment
- Logistic regression training on all four datasets
- Feature standardization using StandardScaler
- Evaluation metrics: accuracy, precision, recall, F1-score
- Confusion matrix analysis for each imputation strategy

### Part C: Comparative Analysis
- Performance comparison across imputation methods
- Class-wise metric analysis (defaulters vs. non-defaulters)
- Visual comparisons with bar plots and heatmaps

## Requirements
- Python 3.x
- Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

## Usage
1. Place `UCI_Credit_Card.csv` in the project directory.
2. Open `Assignment_6.ipynb` in Jupyter and run cells sequentially.
3. Review visualizations and comparative analyses.

## Key Insights
- All imputation strategies yield similar accuracy (~80-81%), indicating minimal impact of imputation method on overall performance.
- Models achieve high precision and recall for non-defaulters but struggle with defaulter recall (~21-22%), likely due to class imbalance.
- Linear regression and decision tree imputation slightly improve recall for defaulters compared to median imputation.
- Choice of imputation strategy has minimal effect on model performance for this dataset.

For detailed analysis, refer to notebook visualizations and observations.
