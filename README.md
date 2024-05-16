# Insurance Premium Prediction Using AutoML

### Overview
This project develops a predictive model to determine the likelihood of on-time premium payments by insurance policyholders. Leveraging automated machine learning (AutoML) technology from H2O.ai, the model is trained on historical data encompassing demographic, financial, and policy-related features of customers. The primary goal is to enhance decision-making processes in insurance operations, focusing on risk management and customer relationship management.

### Dataset Description
The dataset includes the following features:
* id: Unique ID of the policy
* perc_premium_paid_by_cash_credit: Percentage of premium amount paid by cash or credit card
* age_in_days: Age in days of the policyholder
* Income: Monthly Income of the policyholder
* Count_3-6_months_late: Number of premiums late by 3 to 6 months
* Count_6-12_months_late: Number of premiums late by 6 to 12 months
* Count_more_than_12_months_late: Number of premiums late by more than 12 months
* application_underwriting_score: Underwriting Score of the applicant at the time of application (minimum score for insurance is 90)
* no_of_premiums_paid: Total number of premiums paid on time till now
* sourcing_channel: Sourcing channel for the application
* residence_area_type: Area type of Residence (Urban/Rural)
* target: Binary target variable, 1 if the premium was paid on time, 0 otherwise.

### Model Training using AutoML
The project uses H2O's AutoML functionality to automate the process of fitting multiple machine learning models to find the best one based on the AUC metric. The AutoML process is configured with the following parameters:
* max_models: Maximum number of models to build (10 in this case).
* seed: Seed for random number generation to ensure reproducibility.
* verbosity: Debug level set to show detailed logs.
* nfolds: Number of cross-validation folds used for validating the models.

### Best Model
The best performing model from the AutoML process was identified as XGBoost_3_AutoML_1_20230301_04503 with an AUC of 0.836974.

### Model Explanation
Model explanations are provided through the following outputs:
* global_surrogate: A simpler model that approximates the behavior of the best model.
* local_surrogate: Explains predictions for individual instances.
* feature_interactions: Shows interaction effects between features.
* variable_importances: Indicates the importance of each feature in the model.
* feature_impact: Measures the change in model prediction when a feature value is altered.

### Regularization Techniques
The model was regularized using both L1 and L2 techniques to improve model performance and prevent overfitting. Model performance was evaluated using the confusion matrix, and the impact of regularization on model accuracy was assessed.

### Conclusion
This project demonstrates the application of AutoML in predicting insurance premium payments. The insights gained from the model explanations and the impact of regularization techniques help in understanding the factors influencing timely premium payments.



