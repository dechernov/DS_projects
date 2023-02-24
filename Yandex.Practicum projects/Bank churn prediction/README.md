| Project name              | Description   | Libraries used | Status |
| ------------------------- | ------------- | -------------- | ------ |
| Bank churn prediction   | The marketing department of "Beta-Bank" noticed that customers were leaving the bank. It was considered that it is cheaper to keep customers than to attract new ones.| Pandas, scikit-learn, matplotlib | Finished |

**Objective:** develop a binary classification model that predicts whether or not a customer is about to leave the bank based on customer behavior.

**Tasks:** consider and investigate the quality of different binary classification models according to a higher F1 measure with a minimum threshold on a test set of 0.59.

**Summary:** 
* Given the uniform distribution in the `Tenure` column, missing values were filled with values from 0 to 10, taking into account their probability;

* The columns `RowNumber`, `CustomerId` and `Surname` have been deleted because the IDs will always be unique for customers and they have no correlation with the target values. Also, the row number and the last name of the customer are not related to the probability of the customer leaving the bank. It is worth mentioning that using these features to build a model will lead to overfitting;

* The highest F1 metric demonstrated by the random forest fitted on the upsampled set. The F1 metric is ~0.59. ROC-AUC is 0.84, which generally indicates that the built model predicts better than the random model. Random forest hyperparameters are as follows: tree depth - 18, maximum number of features - 2, number of estimators - 110;

* The applicability of the model for a bank is related to the fact that it is cheaper to keep existing customers than to attract new ones. Using the model, it is therefore possible to predict which customers are likely to leave the bank in the near future. This signals to the marketing department that this customer needs to be offered either a rate change or additional services that can retain the customer. However, this requires additional marketing analysis of customer preferences.