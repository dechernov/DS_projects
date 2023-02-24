| Project name              | Description   | Libraries used | Status |
| ------------------------- | ------------- | -------------- | ------ |
| Choosing location for an oil-well   | An oil-producing company is planning to develop a new oil well. It is important to determine the location of the new field.| Pandas, scikit-learn, matplotlib | Finished |

**Objective:** determine the most potentially productive and profitable region.

**Tasks:** create a linear regression model that predicts production volumes for each region. Select the top 200 oil wells with the highest estimated values. Determine the region with the maximum total profit from the selected oil wells.

**Summary:**
* According to the developed logistic regression models and the assessment of investment risk in the development of new oil wells, the most preferable region is Region 1. Despite the high profitability of the 200 best wells for regions 0 and 2 (3.36 and 2.6 billion rubles), region 1 is characterized by the lowest risk (the probability of losses is 0.9%). This is evidenced by the limits of the confidence interval (0.099-0.941 billion rubles), which do not go into negative values, and the average profitability of wells (0.511 billion rubles).
* However, the model may require further adjustment because there are duplicates of oil well IDs in the observations, and there are only 12 unique values for oil wells in region number 1, where there are no completely identical rows.
