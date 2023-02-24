| Project name              | Description   | Libraries used | Status |
| ------------------------- | ------------- | -------------- | ------ |
| Tariff recommendation for a telecommunications company   | A mobile operator plans to analyze customer behavior and offer users of archived tariffs a range of new tariffs: Smart or Ultra.| Pandas, scikit-learn, seaborn| Finished |

**Objective:** develop a classification model that determines the appropriate tariff for a customer based on their behavior.

**Tasks:** research and analyze the quality of different classification models and select one with the highest accuracy metrics on validation and test sets (threshold is 75%).

**Summary:** 
* The highest accuracy in predicting a suitable tariff for a client has a random forest model with the following hyperparameters: the number of estimators - 60, the maximum depth - 10, and the minimum number of samples in a sheet - 6. The accuracy on the test set is 81.3%;

* With this model, the marketing department will be able to determine appropriate plans for new and existing customers based on the analysis of the customer's historical data. In the previous project, the Ultra plan was found to have a higher monthly fee. Therefore, the model also has the potential to maximize revenue per customer.