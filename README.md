# Dataset can be found at:

https://www.kaggle.com/c/home-credit-default-risk/data

# Other resources:

- The entire dataset description and structure can be found in the `home_credit.png` file as well as the `HomeCredit_columns_description.csv` file

# Some Concepts found:

- **AUCROC** or **ROCAUC**: The Reciever Operating Characteristic (ROC) curve graphs the true positive rate versus the false positive rate and AUC is the area under the curve (basically the integral of the curve)
- A curve that is to the left and above another curve indicates a better model.
- The area under the curve (AUC) is always a metric between 0 and 1. a simple guessing random model scores 0.5
- The problem is that of probabilty rather than accuracy.

## EDA results:

- The problem is an class imbalance problem i.e. the total number of a class of data (positive) is far less than the total number of another class of data (negative); in this case the nos. of 1's are way more than the no. of 0's.
- The issue can be further addresed in a more sophesticated way by weighing the classes. Either using XGB boost or sklearn's <a href="https://www.jeremyjordan.me/imbalanced-data/">imabalanced-learn.</a>
- All the missing columns have to undergo imputation or will have to be dropped. Dropping out these columns may lead to poor results.
- Most of the categorical variables have a relatively small number of unique entries.
- These issue of categorical variables can be addressed and solved by encoding.
- Label encoding due to it's arbitary values cannot be used, one-hot encoding is hence used.
- Label encoding is used for 2 categories and one-hot encoding for anything more than that.
