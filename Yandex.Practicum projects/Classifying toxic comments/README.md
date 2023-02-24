| Project name              | Description   | Libraries used | Status |
| ------------------------- | ------------- | -------------- | ------ |
| Classifying toxic comments  | The online store "Wikishop" launches a new service. From now on, users can edit and add to product descriptions in the same way as in wiki communities. This means that customers can offer their own changes and comment on the changes made by others. The store needs a tool to find and moderate toxic comments. | Pandas, scikit-learn, matplotlib, optuna, LightGBM, spaCy| Finished |

**Objective:** develop a machine learning model to classify comments as positive or negative.

**Tasks:** develop several machine learning models to classify comments into positive and negative with a quality metric value (F1) on the test sample of at least 0.75.

**Summary:** 
* The original dataset consists of 150k labeled messages (with or without toxic comments). All messages were converted to lower case, a quick EDA showed a small number of duplicates (45 rows). All messages were processed through the spaCy library, removing unnecessary characters (leaving only letters). For toxic messages, the word cloud shows the most frequent use of words like `piss` and `cocksucker`;
* The target values are characterized by a significant imbalance (~90% non-toxic comments and 10% toxic comments). To deal with the imbalance, we used downsampling and built-in class balancing methods for different models;
* The best model is a logistic regression model trained on the full sample with built-in class balancing methods. The model parameters are as follows: tfidf__min_df = 1, lr__solver = 'sag', lr__C = 3.063462210622083, lr__class_weight = 'balanced'. On the test sample, the F1 metric was ~0.76. This model is much more successful at predicting a toxic comment compared to the constant model (which always predicts class 1).