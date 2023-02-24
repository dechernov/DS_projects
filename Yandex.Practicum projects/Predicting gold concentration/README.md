| Project name              | Description   | Libraries used | Status |
| ------------------------- | ------------- | -------------- | ------ |
| Predicting gold recovery rate from gold-bearing ore   | The company "Cifra" develops various solutions for the efficient operation of industrial enterprises.| Pandas, scikit-learn, matplotlib, optuna, seaborn | Finished |

**Objective:** develop a machine learning model that predicts the recovery rate of gold from gold-bearing ore.

**Tasks:** consider and investigate the quality of different models that predict the recovery rate of gold from gold-bearing ore according to the smallest sMAPE.

**Summary:** 
* The concentration of metals behaves slightly differently at each stage of production. For example, the percentage of silver in the ore after processing is lower than before processing. The median gold content in the initial raw material is less than 10%. At the same time, the gold content increases linearly after each stage of ore cleaning, and at the last stage of cleaning its concentration is about 45%. It is worth noting that the concentration of lead also increases, but its proportion in the final concentrate is the same as that after the first stage of purification;
* Despite the fact that the confidence intervals of the mean values of the pellet sizes do not overlap, the plotted density distribution graphs and whisker boxes show that the distributions are almost identical to each other. In this respect, the data presented can be used for further development of machine learning;
* The total concentration of substances is characterized by a large number of emissions at all stages of production. At the same time, most of the emissions are concentrated below the bottom whisker. Such values were removed from the training and test samples.
* The best model is a random forest model with hyperparameters for rough concentrate: maximum depth: 10, maximum number of features: 'auto', number of trees: 36. For the final concentrate the best model is also a random forest model with hyperparameters: maximum depth: 3, maximum number of features: 'log2', number of trees: 126. The final sMAPE on the test sample was ~6.08;
* After the model is run in production and new data is received, the model may require parameter adjustment.