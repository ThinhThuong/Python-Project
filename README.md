# Python-Project
## I. Context
  Millions of people are denied access to loans because they lack sufficient credit history, leaving them vulnerable to unfair lending practices. Home Credit aims to address this issue by leveraging alternative data sources, such as telco and transactional information, to better predict clients’ repayment ability. 
The challenge is to develop machine learning models that expand financial inclusion by ensuring capable borrowers are approved and provided with fair, supportive loan terms.

## II. Dataset
<img width="1280" height="720" alt="Slide6" src="https://github.com/user-attachments/assets/54701cec-01b2-457c-af08-9c09b117f92e" />
  The dataset is sourced from a Kaggle competition and consists of seven files. However, to address the problem at hand, this project focuses on analyzing the application_{train|test}.csv files. These files are selected because they contain the target label necessary for building machine learning models. The dataset includes over 300,000 rows and 122 features.
<img width="1280" height="720" alt="Slide7" src="https://github.com/user-attachments/assets/bcabe362-84ed-4d9d-be03-ddc564e32416" />
  For model evaluation, the project adopts the AUC-ROC metric to measure predictive performance. 
  Final results will be submitted to the Kaggle competition platform for scoring. The ultimate goal is to identify a machine learning model that ensures clients capable of repayment are not unfairly rejected.

  Since the dataset contains 122 features, analyzing each one individually would be very time-consuming. Therefore, this project includes a literature review to identify which features are commonly reported in research as having significant influence on customers’ loan repayment ability. The reviewed scientific publications includes:

  *1. Sangwan, S., Nayak, N. C., & Samanta, D. (2020). Loan repayment behavior among the clients of Indian microfinance institutions: A household-level investigation. Journal of Human Behavior in the Social Environment, 30(4).*

  *2. Werema, S., & Opanga, K. (2016). Factors affecting clients on loan repayment for microfinance institutions: a case study of PRIDE Arusha, Tanzania. International journal of scientific and technical research in engineering, 1(8).*

  The review of the two research papers indicates that four major factors significantly affect customers’ loan repayment ability: Gender, Age, Educational Attainment, and Occupation Type. 
  The detailed impacts of these factors are presented in the following table.
  
<img width="943" height="423" alt="image" src="https://github.com/user-attachments/assets/16a65380-d965-4dda-9828-9409c1f42129" />
  
  But, How these features affect the customers’ loan repayment ability in the Home Credit's context
  
  <img width="1280" height="720" alt="Slide15" src="https://github.com/user-attachments/assets/415f5941-62dc-4ca8-a6e7-57b75216dfba" />

## III. Insights
### 1. `Gender` feature
  <img width="1280" height="720" alt="Slide17" src="https://github.com/user-attachments/assets/72369139-5a3d-48a0-a3c4-76dffcdb0eb5" />
  Approximately 7% of women experience difficulties in loan repayment, compared to 10% of men. This aligns with Sangwan’s study, which concluded that women generally demonstrate stronger repayment capacity.
  
### 2. `Age` feature
<img width="1280" height="720" alt="Slide18" src="https://github.com/user-attachments/assets/33551016-629c-4b4e-bb3b-d654e677ffdd" />

* Left figure: Loan repayment difficulties are more concentrated among younger customers.

* Right figure: Across age groups, the number of customers struggling with repayment decreases with increasing age.

### 3. `Education level` feature
<img width="1280" height="720" alt="Slide19" src="https://github.com/user-attachments/assets/4a7fe41e-ab65-4a85-8f05-7365fd7154c3" />
In the chart, where the x-axis is ordered from lower to higher education levels, indicates that customers with higher education tend to have fewer repayment difficulties compared to those with lower educational attainment.

### 4. `Occupation type` feature
<img width="1280" height="720" alt="Slide20" src="https://github.com/user-attachments/assets/c9ec9001-1bd6-428f-8656-29308e4076e0" />
The chart illustrates manual occupations in red box and mental occupations in green box, revealing that customers in manual jobs tend to have higher rates of repayment difficulties than those in mental jobs.

### 5. `Score of External` feature
<img width="1280" height="720" alt="Slide21" src="https://github.com/user-attachments/assets/efe657e7-8c2a-4532-a1da-82ed953d6ff3" />
EXT_SOURCE represents the credit scores assigned to individuals by external institutions. 
In both features, repayment difficulties are mainly concentrated in the lower score segments, indicating that customers with lower credit scores are more likely to face challenges in repaying their loans.

## IV. Machine learning model
<img width="1280" height="720" alt="Slide23" src="https://github.com/user-attachments/assets/92f729e4-d451-4c05-b8bd-45a63407082f" />

To predict customers' repayment ability, this project will evaluate several machine learning algorithms to identify the model with the highest prediction accuracy. 
Since the dataset is **highly imbalanced**, accuracy alone is not an appropriate metric. Therefore, the Area Under the Receiver Operating Characteristic Curve (AUC-ROC) will be used as the main evaluation metric for model comparison.

The dataset will be preprocessed through several steps before being used in the machine learning algorithms. The dataset was preprocessed through the following steps:
* Apply Label Encoding for categorical features
* Fill missing values with the median
* Use MinMax Scaler for feature normalization

<img width="1280" height="720" alt="Slide25" src="https://github.com/user-attachments/assets/3fdeb670-28e2-4f21-b0f4-bd821e34236f" />

The machine learning libraries applied in this project include Logistic Regression, LightGBM, and XGBoost.

<img width="1280" height="720" alt="Slide26" src="https://github.com/user-attachments/assets/a1f21d69-ab45-41dd-811d-817e3fe307b5" />

The results show that the AUC scores of LightGBM, XGBoost, and Logistic Regression are 0.75, 0.74, and 0.72, respectively. 
Therefore, LightGBM is considered the most optimal method. After submitting the predictions on Kaggle, the model achieved a score of 0.74307.

<img width="1280" height="720" alt="Slide27" src="https://github.com/user-attachments/assets/e3f27ec3-7e12-46f8-8a7f-cf34665c76a7" />

For the LightGBM model, the most influential features are EXT_SOURCE_3, DAYS_BIRTH, and EXT_SOURCE_1. Therefore, these three features can be used for preliminary analysis to predict whether a customer is likely to experience difficulties in loan repayment. 
The importance of these features is intuitive: credit scores (EXT_SOURCE) directly reflect customers’ creditworthiness, while age (DAYS_BIRTH) often correlates with financial stability and repayment behavior.

## V. Conclusion
<img width="1280" height="720" alt="Slide29" src="https://github.com/user-attachments/assets/5afe2c22-ef1f-45ab-bb23-683473e349b5" />

Based on the analysis, several key factors were found to strongly influence customers’ loan repayment ability. In addition, different machine learning models were compared to identify the most effective approach for prediction.
Key factors influencing repayment ability:
* Gender: Male
* Age: Youth
* Level of Education: Lower education
* Occupation Type: Physical jobs
* External Score: Low score
Best performing model: LightGBM – most effective in predicting customers’ repayment capacity
Business implication: These insights can help lenders design more accurate credit risk assessment strategies and provide fairer access to loans for customers capable of repayment.
