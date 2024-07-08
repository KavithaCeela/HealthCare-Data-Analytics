# Healthcare Analytics Capstone Project

## Table of Contents
1. Introduction
2. Project Goal
3. Hypothesis Generation
4. Data Exploration
   - Data Overview
   - Data Cleaning and Preparation
   - Feature Engineering
5. Modeling Strategy
   - Model 1 - Naïve Bayes
   - Model 2 - XGBoost
   - Model 3 - Neural Networks
6. Predictions and Results
7. Future Insights
8. Conclusion

## Introduction
Healthcare organizations are under increasing pressure to improve patient care outcomes and achieve better care. This project focuses on leveraging data analytics to predict patient length of stay (LOS) in hospitals, which can help optimize treatment plans, reduce infection rates, and manage hospital resources more effectively.

## Project Goal
The goal of this project is to accurately predict the Length of Stay for each patient so that hospitals can optimize resources and function better.

## Hypothesis Generation
We generated hypotheses by considering different factors that might impact the Length of Stay. These factors were divided into two levels:
- **Patient-Level:** Type of Admission, Severity of Illness, Visitors with Patient, Age, Admission Deposit
- **Hospital-Level:** Ward Type, Department

## Data Exploration
### Data Overview
The dataset consists of 318,438 observations with 17 variables. The target variable is the length of stay (Stay), which is divided into 11 different classes ranging from 0 days to more than 100 days.

### Data Cleaning and Preparation
- Missing values in `City_code_patient` and `Bed Grade` were imputed using the mode imputation technique.
- Ordinal variables were transformed using label encoding.

### Feature Engineering
We engineered new features such as `count_id_patient`, `count_id_patient_hospitalCode`, and `count_id_patient_wardfacilityCode` to capture the count of multiple admissions and ward allocations.

## Modeling Strategy
We implemented three models to predict the Length of Stay:

### Model 1 - Naïve Bayes
A Gaussian Naïve Bayes classifier was used, achieving an accuracy of 34.55%.

### Model 2 - XGBoost
An XGBoost classifier with tuned hyperparameters was implemented, achieving an accuracy of 43.04%.

### Model 3 - Neural Networks
A neural network with six dense layers was implemented, achieving an accuracy of 42.05%.

## Predictions and Results
- Naïve Bayes showed bias towards a specific LOS range.
- XGBoost and Neural Networks provided more accurate and similar predictions.
- The distribution of predictions showed that most patients stay for 21-30 days, while very few stay for 61-70 days.

## Future Insights
- **Smart Staffing & Personnel Management:** Allocate resources efficiently based on data insights.
- **Advanced Risk & Disease Management:** Offer preventive care by analyzing various factors.
- **Real-time Alerting:** Use Clinical Decision Support (CDS) to deliver recommendations on the spot.
- **Enhancing Patient Engagement:** Track health metrics to identify potential risks.

## Conclusion
Predicting patient Length of Stay can help hospitals allocate resources efficiently and manage patients effectively, reducing overall medical expenses.
