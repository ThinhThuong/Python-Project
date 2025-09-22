# Python-Project
## Context
Millions of people are denied access to loans because they lack sufficient credit history, leaving them vulnerable to unfair lending practices. Home Credit aims to address this issue by leveraging alternative data sources, such as telco and transactional information, to better predict clients’ repayment ability. 
The challenge is to develop machine learning models that expand financial inclusion by ensuring capable borrowers are approved and provided with fair, supportive loan terms.

## Dataset
<img width="1280" height="720" alt="Slide6" src="https://github.com/user-attachments/assets/54701cec-01b2-457c-af08-9c09b117f92e" />
The dataset is sourced from a Kaggle competition and consists of seven files. However, to address the problem at hand, this project focuses on analyzing the application_{train|test}.csv files. These files are selected because they contain the target label necessary for building machine learning models. The dataset includes over 300,000 rows and 122 features.
<img width="1280" height="720" alt="Slide7" src="https://github.com/user-attachments/assets/bcabe362-84ed-4d9d-be03-ddc564e32416" />
For model evaluation, the project adopts the AUC-ROC metric to measure predictive performance. Final results will be submitted to the Kaggle competition platform for scoring. The ultimate goal is to identify a machine learning model that ensures clients capable of repayment are not unfairly rejected.
