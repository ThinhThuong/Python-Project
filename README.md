# Python-Project
## Context
Millions of people are denied access to loans because they lack sufficient credit history, leaving them vulnerable to unfair lending practices. Home Credit aims to address this issue by leveraging alternative data sources, such as telco and transactional information, to better predict clients’ repayment ability. 
The challenge is to develop machine learning models that expand financial inclusion by ensuring capable borrowers are approved and provided with fair, supportive loan terms.

## Dataset
<img width="1280" height="720" alt="Slide6" src="https://github.com/user-attachments/assets/54701cec-01b2-457c-af08-9c09b117f92e" />
The dataset is sourced from a Kaggle competition and consists of seven files. However, to address the problem at hand, this project focuses on analyzing the application_{train|test}.csv files. These files are selected because they contain the target label necessary for building machine learning models. The dataset includes over 300,000 rows and 122 features.
<img width="1280" height="720" alt="Slide7" src="https://github.com/user-attachments/assets/bcabe362-84ed-4d9d-be03-ddc564e32416" />
For model evaluation, the project adopts the AUC-ROC metric to measure predictive performance. 
Final results will be submitted to the Kaggle competition platform for scoring. The ultimate goal is to identify a machine learning model that ensures clients capable of repayment are not unfairly rejected.

Since the dataset contains 122 features, analyzing each one individually would be very time-consuming. Therefore, this project includes a literature review to identify which features are commonly reported in research as having significant influence on customers’ loan repayment ability. The reviewed scientific publications includes:

*1. Sangwan, S., Nayak, N. C., & Samanta, D. (2020). Loan repayment behavior among the clients of Indian microfinance institutions: A household-level investigation. Journal of Human Behavior in the Social Environment, 30(4).*

*2. Werema, S., & Opanga, K. (2016). Factors affecting clients on loan repayment for microfinance institutions: a case study of PRIDE Arusha, Tanzania. International journal of scientific and technical research in engineering, 1(8).*

The literature review highlights four major determinants of customers’ loan repayment ability: `Gender`, `Age`, `Educational Attainment`, and `Occupation Type`.
<img width="943" height="423" alt="image" src="https://github.com/user-attachments/assets/16a65380-d965-4dda-9828-9409c1f42129" />

