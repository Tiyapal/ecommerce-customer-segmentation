# E-Commerce Customer Segmentation

## Project Overview

This project is an AI & ML capstone project focused on analyzing and segmenting e-commerce customers based on their demographic, transactional, behavioral, engagement, and customer-value characteristics.

The project explores customer patterns and uses machine learning techniques to classify customers according to their risk level, with particular focus on identifying high-risk customers.

The objective is to demonstrate practical understanding of data analysis, exploratory data analysis, preprocessing, machine learning, model evaluation, and customer-focused business insights.

## Dataset

The dataset contains 50,000 customer records and 53 variables.

The dataset includes information related to:

- Customer demographics
- Purchase behavior
- Customer satisfaction
- Complaints and returns
- Customer engagement
- Transactional activity
- Customer lifetime value
- Customer profitability
- Customer segmentation
- Churn risk

## Project Workflow

The project follows these major steps:

1. Dataset loading and understanding
2. Data quality analysis
3. Missing-value analysis
4. Duplicate-value analysis
5. Target variable creation
6. Exploratory Data Analysis (EDA)
7. Outlier analysis
8. Correlation analysis
9. Feature selection
10. Train-test split
11. Data preprocessing
12. Machine learning model training
13. Model evaluation
14. Confusion matrix analysis
15. Train vs. test performance analysis
16. Model comparison
17. Final model selection
18. Business interpretation

## Customer Risk Classification

The dataset contains a `churn_risk_category` variable with five risk levels:

- Very Low
- Low
- Medium
- High
- Very High

For the machine learning classification task, a binary target variable called `high_risk_flag` was created.

Customers classified as **High** or **Very High** risk are assigned:

- `1` = High Risk
- `0` = Not High Risk

This classification helps identify customers who may require greater attention from a customer-management and retention perspective.

## Exploratory Data Analysis

The EDA process was used to identify important patterns and relationships within customer data.

Important observations include:

- High-risk customers have substantially higher values of `days_since_last_purchase`.
- High-risk customers have lower satisfaction scores.
- High-risk customers tend to have more complaints and returns.
- RFM-related measures decrease as customer risk increases.
- Several numerical variables contain outliers.
- The high-risk classification is imbalanced, with high-risk customers representing a smaller proportion of the dataset.

## Machine Learning Models

Two classification algorithms were implemented.

### 1. Logistic Regression

Logistic Regression was selected as a baseline classification model because it is simple, interpretable, and suitable for binary classification.

### 2. Random Forest

Random Forest was selected because it can capture nonlinear relationships and interactions between customer-related features and is suitable for classification problems involving multiple features.

## Data Preprocessing

The preprocessing pipeline includes:

- Median imputation for numerical missing values
- Most-frequent imputation for categorical missing values
- Standard scaling of numerical variables
- One-hot encoding of categorical variables

The preprocessing steps were incorporated into machine learning pipelines to ensure consistent processing of training and testing data.

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

Because the target variable is imbalanced, accuracy was not considered sufficient on its own. Precision, recall, F1-score, and ROC-AUC were also used for a more complete evaluation.

## Results

### Logistic Regression

- Test Accuracy: 92.27%
- Test Precision: 40.44%
- Test Recall: 91.30%
- Test F1-score: 56.06%
- Test ROC-AUC: 97.53%

### Random Forest

- Test Accuracy: 97.25%
- Test Precision: 75.14%
- Test Recall: 73.33%
- Test F1-score: 74.23%
- Test ROC-AUC: 98.23%

## Final Conclusion

Random Forest achieved better overall test performance than Logistic Regression, with higher test accuracy, precision, F1-score, and ROC-AUC.

Logistic Regression achieved higher recall and showed a smaller difference between training and testing performance. This indicates more consistent generalization and a stronger ability to identify actual high-risk customers.

Based on the overall evaluation, **Random Forest was selected as the stronger overall predictive model**, while Logistic Regression remains useful when maximizing high-risk customer detection is the primary objective.

## Business Impact

The analysis can help an e-commerce business:

- Understand different customer characteristics and behavioral patterns
- Identify customers who are at higher risk
- Prioritize customer-retention strategies
- Identify patterns associated with customer risk
- Support data-driven customer relationship management
- Improve customer segmentation and decision-making

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Files

- `Skill Ladders AI-ML Capstone.ipynb` - Complete project notebook containing data analysis, preprocessing, machine learning, evaluation, visualizations, and conclusions.
- `E-commerce_Customer_Segmentation_2026.csv` - Dataset used for the project.
- `README.md` - Project documentation.

## Author

**Jayeeta Pal**

**Domain:** AI & ML