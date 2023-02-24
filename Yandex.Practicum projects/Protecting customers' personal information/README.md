| Project name              | Description   | Libraries used | Status |
| ------------------------- | ------------- | -------------- | ------ |
| Protecting customers' personal information   | insurance company plans to use data encryption to keep personal information secure.| Pandas, scikit-learn, numpy| Finished |

**Objective:** protect user data from leaks as the company develops machine learning models.

**Tasks:** develop a method for transforming user data to make it harder to recover personal information, while not degrading the quality of machine learning models.

**Summary:** 
* During the development of the encryption algorithm for user data, explicit duplicates were detected. The presence of duplicates may be due to a technical error during data download.

* The target value is the column that characterizes the number of insurance payments to the client in the last 5 years. The remaining columns are characteristics and characterize socio-demographics (gender, age, number of family members) and consumer profile (client's salary). All of this is user data that must be encrypted.

* As an algorithm for user data encryption, the multiplication of features by an invertible random matrix should be used. In this case, the quality of the linear regression model will not change due to the reversibility property of the random matrix. The product of a random matrix and an invertible matrix is equal to the identity matrix, and its multiplication by any other matrix leaves the identity matrix unchanged.