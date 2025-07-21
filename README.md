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

## Key Insights
+ Top predictors: tenure, MonthlyCharges, Contract, InternetService, and PaymentMethod were the most influential in predicting customer churn, with tenure being the strongest.

+ SMOTE significantly improved recall (0.84), enhancing the model’s ability to detect customers likely to churn.

+ Feature Importance Plot highlighted key churn drivers, enabling targeted retention strategies. Incorporating SHAP values is recommended for deeper interpretability and fairness assessment.

+ Confusion Matrix confirmed reliable prediction distribution, supporting automation of churn risk detection.

+ ROC Curve demonstrated strong model performance, with Random Forest achieving an AUC of 0.943, outperforming baseline models like Logistic Regression.

## Conclusion
## Conclusion
###  1.Improved Churn Prediction Accuracy
The optimized Random Forest model effectively captures customer behavior patterns, leveraging features like customer service calls, international plan, and usage metrics for accurate churn prediction.

###  2.Enhanced Churn Risk Detection
Addressing class imbalance using SMOTE significantly improves the model's ability to identify high-risk customers, reducing missed churners and enabling timely retention strategies.

###  3.Customer-Centric Decision-Making
Encoding features such as state, account length, and plan subscriptions allows for deeper segmentation and potential bias analysis. However, further fairness evaluation is essential to ensure equitable treatment of all customer groups.

###  4.Efficient, Scalable Deployment
Model automation using joblib facilitates seamless deployment of the churn model, enhancing operational efficiency and enabling proactive customer engagement at scale.

###  5.Transparent Model Interpretability
Feature importance analysis highlights the most influential churn drivers, improving trust and communication with stakeholders and supporting data-driven decisions.

###  6.Key Predictors & Business Insights

* Customer Service Calls: Strongest indicator of potential churn.

* Usage Metrics (e.g., Day Minutes/Charges): Reflect customer engagement and satisfaction.

* Plan Subscriptions (e.g., International & Voice Mail): Offer insight into service value.

* Account Longevity & Location: Contribute to customer profiling and experience assessment.

###  7.Alignment with Business Goals
The model strengthens churn prediction accuracy, enables targeted retention efforts, supports equity in treatment, and enhances operational efficiency—advancing strategic goals for customer lifecycle management.

###  8.Future Improvements
Ongoing efforts such as performance monitoring, threshold tuning, and applying fairness metrics will further refine model performance while maintaining ethical standards in customer management.