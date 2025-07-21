# Customer-Churn-Predictor
## Overview
 This project develops a machine learning model to predict customer churn (churn: 1 = will churn, 0 = will stay) using historical telecom customer data. The model aims to help businesses proactively identify at-risk customers and take targeted actions to improve retention.

 We use a Random Forest Classifier, optimized using RandomizedSearchCV, to achieve high predictive performance. The project addresses class imbalance with SMOTE, ensures fairness, supports business-driven decisions, and emphasizes model interpretability.
   
## Objectives
* Improve Customer Retention Accuracy
Build a robust model to accurately predict which customers are likely to churn (leave the service).

* Minimize Revenue Loss
Identify high-risk churn customers early to enable proactive retention strategies and reduce revenue leakage.

* Support Data-Driven Retention Campaigns
Provide actionable insights to guide personalized offers, loyalty programs, and customer engagement efforts.

* Promote Fairness and Inclusivity
Analyze churn risk across demographic groups to detect and mitigate potential biases in predictions.

* Enable Scalable and Automated Decision-Making
Integrate the model into customer relationship management (CRM) systems for real-time churn flagging and automation.

* Ensure Interpretability and Transparency
Use feature importance and visual explanations to help stakeholders understand and trust model outputs.

## Key Features
* Dataset: ~7,040 rows with features such as tenure, MonthlyCharges, Contract, PaymentMethod, InternetService, and Churn.

* Preprocessing:

+ Handled class imbalance using SMOTE applied only to the training set.

+ One-hot encoding for categorical variables like Contract, PaymentMethod, and InternetService.

+ Outlier handling applied to numerical features using IQR and capping strategies.

* Model:

+ Random Forest Classifier (best_rf) optimized using RandomizedSearchCV.

+ Model saved as random_forest_churn_model.joblib.

* Evaluation Metrics:

+ Accuracy: 0.96

+ Precision: 0.93

+ Recall: 0.84

+ F1 Score: 0.88

+ ROC AUC: 0.943

* Visualizations:

+ Feature Importance Plot – highlights key drivers of churn such as tenure, MonthlyCharges, and Contract.

+ Confusion Matrix – shows classification performance and distribution of false positives/negatives.

+ Precision-Recall Curve – used for optimal threshold tuning.

+ ROC Curve – visualizes trade-off between TPR and FPR.

+ (Optional) SHAP/ELI5 explanations – (insert if added later).