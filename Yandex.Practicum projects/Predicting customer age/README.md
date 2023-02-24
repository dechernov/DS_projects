| Project name              | Description   | Libraries used | Status |
| ------------------------- | ------------- | -------------- | ------ |
| Predicting customer age   | A supermarket is implementing a computer vision system to process customer photos. Photofixation at checkout will help determine customer age to analyze purchases and offer goods that may be of interest to customers in that age group, as well as to monitor cashiers when selling alcoholic beverages.| Pandas, Keras, matplotlib, seaborn| Finished |

**Objective:** train a neural network to determine the approximate age of a customer from a photo.

**Tasks:** perform exploratory data analysis, data preparation for training, train the neural network, and calculate the quality of the network.

**Summary:** 
* The total number of photos is 7,591. The histogram of age groups is characterized by a long tail and the distribution is skewed to the right. 75% of the observations are concentrated at ages below 41 years. Note the outliers in observations around the ages of 25, 30, 40, 50, 60, 70, 80, and 90. The exact person's age in the photo was unknown and the number was rounded;
* The photos in the dataset are mostly in color. However, there are also black and white images. In some of the photos, foreign objects are also observed at the level of the face. The accuracy of the built model may be reduced by these objects. The photos were not adjusted to the vertical position. The neural network was built based on the ResNet architecture with ImageNet weights, the backbone was not frozen. There is one output neuron (customer's age);
* The final error of the constructed neural network is 6.6 years, i.e. the average model error is 6.6 years in both directions. This is less than the required value (8 years). As expected, this value is not critical for determining the age category of the buyer. However, this error is too high to control cashiers at the checkout zone when selling alcoholic beverages. We should also note the model overfitting, on the training set there is a significant improvement in the MAE, while on the validation set, there is a slight metric improvement;
* The model can be improved by adding photos of people aged 10-20 years. We can also add functionality to the model to determine if a person can be sold alcohol and if additional verification is needed.