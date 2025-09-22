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

  The review of the two research papers indicates that four major factors significantly affect customers’ loan repayment ability: Gender, Age, Educational Attainment, and Occupation Type. 
  The detailed impacts of these factors are presented in the following table.
  
<img width="943" height="423" alt="image" src="https://github.com/user-attachments/assets/16a65380-d965-4dda-9828-9409c1f42129" />
  
  But, How these features affect the customers’ loan repayment ability in the Home Credit's context
  
  <img width="1280" height="720" alt="Slide15" src="https://github.com/user-attachments/assets/415f5941-62dc-4ca8-a6e7-57b75216dfba" />

## Insights
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

## Machine learning model



