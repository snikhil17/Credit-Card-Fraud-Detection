# Credit-Card-Fraud-Detection
- Project is made as a final team project during the course Data Science ML & DL by [REGex Software Services](https://www.regexsoftware.com/) 

## [ABSTRACT](https://github.com/snikhil17/Credit-Card-Fraud-Detection/tree/main/0.%20Notebooks%20and%20Report)
It is important that credit card companies are able to recognize fraudulent
credit card transactions so that customers are not charged for items that
they did not purchase. The challenge is to recognize fraudulent credit
card transactions so that the customers of credit card companies are not
charged for items that they did not purchase.

## [CONSTRAINTS](https://github.com/snikhil17/Credit-Card-Fraud-Detection/tree/main/0.%20Notebooks%20and%20Report)
**Main challenges involved in credit card fraud detection are:**
- Enormous Data is processed every day and the model build must be fast enough to respond to the scam in time.
- Imbalanced Data i.e. most of the transactions (99.8%) are not fraudulent which makes it really hard for detecting the fraudulent ones
- Data availability as the data is mostly private.
- Miss-classified Data can be another major issue, as not every fraudulent transaction is caught and reported.
- Adaptive techniques used against the model by the scammers.

**How to tackle these challenges?**
- The model used must be simple and fast enough to detect the anomaly and classify it as a fraudulent transaction as quickly as possible.
- Imbalance can be dealt with by properly using some methods which is explained in the notebook and porject report in detail.
- For protecting the privacy of the user, the dimensionality of the data can be reduced.
- A more trustworthy source must be taken which double-checks the data, at least for training the model.
- We can make the model simple and interpretable so that when the scammer adapts to it with just some tweaks, we can have a new model up and running to deploy.

## [PROJECT APPROACH](https://github.com/snikhil17/Credit-Card-Fraud-Detection/tree/main/0.%20Notebooks%20and%20Report)
- **Data Acquisition:** Collected data from research (http://mlg.ulb.ac.be) of ULB (Université Libre de Bruxelles).
- **Exploratory Data Analysis (EDA):**
  - Missing Value and Duplicates
  - Variable Distribution
  - Outlier Treatment
  - Correlation
  - Impact of Imbalanced data by training and comparing 3 models (Isolation Forest, Local Outlier Factor and SVM)
- **Preprocessing:**
  - Standardized Amount and Time variable
  - Using SMOTETomek to take care of unbalanced data.
  - Used train_test_split with stratify parameter was to maintain the imbalanced proportion of data.
- Hyper-parameter tuning using **Optuna** - Random Forest, XGBoost and MLPClassifier(NN). **Evaluation used roc_auc_score**
- Build Model using parameters obtained from Optuna hyper-parameter tuning.
- **Final model used: Voting Classifier with soft voting mode**, which considers the - probabilities thrown by each ML model, these probabilities will be weighted and
averaged, consequently the winning class will be the one with the highest weighted and averaged probability.

## TEAM INFORMATION:
- Nikhil Shrestha: AIRSS1129
- Maneesh Arava: AIRSS1142
- Y. Manohar Reddy: AIRSS1139
- Furzana J: AIRSS1132
- Afzal Vali: AIRSS1138

