# Employee Attrition Prediction using Decision Tree and Random Forest
**Author:** Arnav Tripathi

**Registration Number:** 23BCE10756  
**Application Number:** IN26011416  
**Batch Number:** 2B  
**Email ID:** arnav.23bce10756@vitbhopal.ac.in

## Objective
The objective of this project is to build Decision Tree and Random Forest classification models to accurately predict employee attrition based on demographic, professional, and work-related attributes.

## Dataset Link
Kaggle: IBM HR Analytics Employee Attrition & Performance Dataset

link: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset

## Libraries Used
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Methodology
- **Data Understanding:** Identified numerical and categorical features along with the target variable (`Attrition`), and inspected the dataset's summary statistics.
- **Data Preprocessing:**
  - Checked for missing values.
  - Dropped unnecessary columns (`EmployeeCount`, `EmployeeNumber`, `Over18`, and `StandardHours`).
  - Encoded all categorical variables using `LabelEncoder`.
  - Split the dataset into 80% training and 20% testing sets using stratified sampling on the target variable.
- **Model Development:** Trained a `DecisionTreeClassifier` and a `RandomForestClassifier` (with 100 estimators) on the training features.
- **Model Evaluation:** Evaluated both models using Accuracy, Precision, Recall, and F1-Score. Generated Confusion Matrices for both models and a Feature Importance plot for the Random Forest.

## Results
**Decision Tree Performance:**
- **Accuracy:** 78.23%
- **Precision:** 31.91%
- **Recall:** 31.91%
- **F1-Score:** 0.3191

**Random Forest Performance:**
- **Accuracy:** 84.35%
- **Precision:** 54.55%
- **Recall:** 12.77%
- **F1-Score:** 0.2069

## Conclusion
The Random Forest model outperformed the Decision Tree in terms of overall accuracy (84.35%) and precision (54.55%). Random Forests generally outperform individual Decision Trees because they aggregate the predictions of multiple trees trained on random subsets of data and features, which reduces variance and prevents overfitting. However, the Decision Tree achieved better recall (31.91%), meaning it caught more of the employees who actually left. 

A primary limitation of Decision Trees is their tendency to overfit the training data and memorize noise. On the other hand, the main limitation of the Random Forest model is its lack of interpretability; an ensemble of 100 trees is much harder to visualize and explain to stakeholders compared to a single decision tree.
