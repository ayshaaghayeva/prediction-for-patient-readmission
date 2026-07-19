# Prediction for Patient Readmission

## Target Framing

The original `readmitted` variable was converted into a binary target, where patients readmitted within 30 days were labelled as the positive class and all other cases as the negative class. This framing focuses on predicting early hospital readmission.

## Data Handling

The dataset was cleaned by handling missing values, removing unnecessary identifiers, encoding categorical variables, and checking for potential data leakage. A patient-level train-test split was used to ensure that records from the same patient did not appear in both the training and testing sets.

## Class Imbalance Handling

The target variable was imbalanced. Class weights were applied in Logistic Regression, and `scale_pos_weight` was used in XGBoost to improve the detection of early readmission cases.

## Baseline Comparison

Logistic Regression was used as the baseline model and compared with XGBoost. Both models were evaluated using the same training and testing data. XGBoost achieved a slightly higher recall and F1-score, making it the preferred model.

## Evaluation

Model performance was evaluated using Accuracy, Precision, Recall, F1-score, the Confusion Matrix, and the Classification Report. Because the dataset was imbalanced, greater emphasis was placed on Recall and F1-score rather than Accuracy alone.

## SHAP Trust Conclusion

SHAP was used to explain the XGBoost model. The analysis showed that the model mainly relied on clinically meaningful features, including previous inpatient visits, number of diagnoses, length of hospital stay, and diabetes-related information. The feature `discharge_disposition_id` was also influential and should be interpreted carefully because it may introduce data leakage if used inappropriately.

## Fairness Analysis

A fairness analysis was conducted to evaluate model performance across gender, race, and age groups using recall. The results showed generally consistent performance across demographic groups, although some variation was observed across certain race and age categories.

