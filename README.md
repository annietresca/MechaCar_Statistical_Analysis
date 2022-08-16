# MechaCar_Statistical_Analysis

## Overview of the Analysis

This report contains three analyses as well as a proposal:

Deliverable 1: Linear Regression to Predict MPG

Deliverable 2: Summary Statistics on Suspension Coils

Deliverable 3: T-Test on Suspension Coils

Deliverable 4: Design a Study Comparing the MechaCar to the Competition

## Resources

Software: R studio

## Linear Regression to Predict MPG
Using the MechaCar_mpg.csv file, I created a linear regression model that predicts the mpg of prototypes. 
![Deliverable 1](https://github.com/annietresca/MechaCar_Statistical_Analysis/blob/main/Images/Deliverable%201%20pvalue.png) 

Based on the above image and linear regression model:

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset? The intercept, vehicle_length and ground_clearance variables/coefficients provided non-random amounts of variance to the mpg values.

2. Is the slope of the linear model considered to be zero? Why or why not? The slope of this linear model is not considered to be zero. This can be determined by looking at the p-value of this analysis, which, according to this model is 5.35 e-11. Because this is significantly smaller than the 0.05 significance level of the null hypothesis, we can safely say the slope is not equal to zero. 

3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not? The adjusted R squared value of this linear regression is 0.6825 which means that the linear model predicts mpg effectively.

## Summary Statistics on Suspension Coils
Using the Suspension_coil.csv file, I created two dataframes that assess the testing weight capabilites of different suspension coils in order to determine consistency.

Total Summary:

![Total Summary](https://github.com/annietresca/MechaCar_Statistical_Analysis/blob/main/Images/total%20summary.png)

Lot Summary:

![Lot Summary1](https://github.com/annietresca/MechaCar_Statistical_Analysis/blob/main/Images/lot%20summary1.png)

![Lot Sumamry2](https://github.com/annietresca/MechaCar_Statistical_Analysis/blob/main/Images/lot%20summary%202.png)

Based on the above images and summary statistics:

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not? 

Overall, the variance for the entire dataset demonstrates that the current manufacturing data meets the 100 pounds per square inch variance limitation. Individually, things are more nuanced. Lot 1 and Lot 2 meet the design specifications with variances of 0.97 and 7.47. However, Lot 3's variance is 170.28 which is significant, especially when compared to the other Lots in the data set. This would cause me to assess that the third lot has a possibility of not meeting the necessary suspension coils requirements.


## T-Tests on Suspension Coils
Using the Suspension_coil.csv file, I created t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.


![ttest 1](https://github.com/annietresca/MechaCar_Statistical_Analysis/blob/main/Images/true%20mean.png)

As can be seen above, the p-value of the dataset is 0.06 which indicates that we have failed to reject the null hypothesis (0.05). Because of this, we cannot say that the sample mean isnt equal to the true population mean. 

![ttest2](https://github.com/annietresca/MechaCar_Statistical_Analysis/blob/main/Images/t%20tests.png)

Lot 1: Has a p-value of 1 which means we fail to reject the null hypothesis.

Lot 2: Has a p-value of 0.60 which means we again fail to reject the null hypothesis.

Lot 3: Has a p-value of 0.04 which means we can reject the null hypothesis. As a result, we can say that the sample mean and the (presumed) population mean are not statistically different. 


## Study Design: MechaCar vs Competition

As part of a follow up study, it would be interesting to utilize a linear regression model on fuel efficiency, for both city and highway respectively and compare MechaCar's standing against the competition. Given the astronomical fuel costs as of late, this could prove pivotal in bringing in new customers!

### Metrics:
- MPG (city and highway) dependent variable(s) 
- Fuel Capacity/Type independent variable
- AWD abilities independent variable
- Horsepower indepdendent variable

### Null Hypothesis:
The MechaCar is not priced appropriately for its fuel efficiency as compared to competitors. 

### Statistical Tests Needed:
A linear regression model would be best for this analysis because it will look to see what variables are most closely correlated and predict the best fuel efficiency and impact on price.

### Data Needed:
MechaCar data as well as current auto competition data
