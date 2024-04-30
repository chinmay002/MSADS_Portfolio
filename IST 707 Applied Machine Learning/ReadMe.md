# CREDIT CARD FRAUD DETECTION 

## Data
  https://github.com/jbofill10/C1_Transaction_Data/tree/master/Data

## Exploratory Data Analysis (EDA)
![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/51a92735-29ab-40e3-83ad-9af70bf44c54)

![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/6fa8fd71-4d96-4c4a-8221-63655cf65ba5)

### Target distribution
![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/5e7d6ee0-d4b7-4633-a252-94fa984dd54a)

### Account with most fradulent transcation
![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/34c5cd74-7108-4be6-9523-43f452966285)

### Amount Distribution
![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/8596c537-bea8-4eb0-9a17-adf8d0cbb921)

## Data Pre-Processing:
The following are the steps I followed to pre-process the data :
• Remove unwanted fields : The dataset had some fields which was entirely NAN. In addition to that some
variables are irrelevant for model training. The following fields are omitted : 'echoBuffer',
'cardLast4Digits','merchantName','accountOpenDate','transactionDateTime','currentExpDate','customerId','dat
eOfLastAddressChange','accountNumber','enteredCVV','cardCVV'.
• Adding derived features : In case of a brute-force attempt to crack the card-CVV, incorrect CVV may be
entered initially. This is an indicator of attempted fraud. So, I am creating a new variable: matchingCVV
which denotes whether the real CVV and entered CVV are same.
• Boolean variables are converted to binary integer (0:False, 1:True) values.
• Categorical values are One-Hot encoded.
• Numerical values, along with the other converted values are normalised using standard scaler.
• The data set is split into features and labels : labels being the isFraud column.
• The dataset is split into 80% for training and 20% for testing.
• Random forest and Logistic regression models are trained on the training data and tested on the testing data.
• Accuracy, Precision, Recall, F1-score are examined, and results are visualised using a confusion matrix.


## Modelling  and Results
![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/c4512cf1-5118-4629-addb-dfc71fd2ed61)

![image](https://github.com/chinmay002/MSADS_Portfolio/assets/60249099/2190383b-a324-4a37-a927-e77b48885f4a)

## Inferences and Insights:
• With respect to accuracy, precision, recall and F1-score, all models seemed to be heavily overfitting and a
plausible comparison couldn’t be drawn.
• However, AUPRC score clearly displayed the performance trend where XG-Boost algorithm performed the
best, and decision tree the least.
• SVM however was not able to fit the data at all, as suggested by the ROC curve.
• We conclude that a single classification algorithm alone may not be efficient enough to classify credit
card fraud, where are ensemble methods show improved performance
