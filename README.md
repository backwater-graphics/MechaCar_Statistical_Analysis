# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

![linear Regression]( https://github.com/backwater-graphics/MechaCar_Statistical_Analysis/blob/main/images/linear_regression_summary.jpg)
---

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
  -  Vehicle weight, spoiler_angle & AWD provided a non-random amount of variance. The two variables that had the most amount of random variance are ground_clearance and vehicle_length.
- Is the slope of the linear model considered to be zero? Why or why not?
  -  Our slope is not zero just be looking at the p-value, which is less than 0.05, we are able to reject the null hypothesis because of the extremely small p-value. The null hypothesis of a linear regression states that the slope (β1) is equal to 0. However, if we reject the null hypthesis, we're stating that alternative (β1 ≠ 0) is true. Thus, proving that the slope is not 0.
- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
  -  From our linear regression model, the r-squared value is 0.7149, which means that roughly 71% of the variablilty of our dependent variable (MPG) is explained using this linear model. While this is fairly predictive, our Intercept is also statistically significant (p= 5.08e-08), so 1) the significant features (vehicle length and ground clearance) may need scaling or transforming to help improve the predictive power of the model, and/or 2) there may be other variables that can help explain the variability of MPG that have not been included in our model.

## Summary Statistics on Suspension Coils

Below is the summary statistics of all of the manufacturing lots. The mean is 1498.78 for this sample and the population mean was determined to be 1500.

![ total_summary]( https://github.com/backwater-graphics/MechaCar_Statistical_Analysis/blob/main/images/total_summary.jpg)
---
 
 The means of the lot numbers are similar to the population mean and the sample mean.
 
![ lot_summary]( https://github.com/backwater-graphics/MechaCar_Statistical_Analysis/blob/main/images/Lot_summary.jpg)
---


- Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
  -  The variance for the total manufacturing lot is 62 < 100, which is within the expected design specifications of staying under 100 PSI. However, when reviewing the data by Lot number, Lot 3 is a large contributing factor to the variance being high. Lot 3 shows a variance of 170 > 100 and does not meet the design specifications. Lot 1 and Lot 2 have significantly lower variance, 1 and 7 respectively.

## T-Tests on Suspension Coils

![ t_test]( https://github.com/backwater-graphics/MechaCar_Statistical_Analysis/blob/main/images/lot_t_tests.jpg)
---

Some T-Tests were performed comparing all manufacturing lots (in total) against the known mean PSI of the data population (1500 psi). T-tests were also performed against the population mean PSI (1500 psi) for each individual manufacturing lot. After thorough review we see that across all lots, the t-tests revealed a mean PSI of 1498.78, which was NOT statistically different (p-value = 0.06028) from the population mean PSI of 1500 psi. Similarly, Manufacturing Lot 1 (with a mean of 1500 PSI and a p-value of 1) and Manufacturing Lot 2 (with a mean of 1500.2 PSI and a p-value of 0.6072) were NOT statistically different from the population mean PSI of 1500. Manufacturing Lot 3 (with a mean of 1496.14 PSI and a p-value of 0.04168), however, was found to be statistically significantly different from the population mean PSI.

## Study Design: MechaCar vs Competition

We performed a statistical comparison of car brands based on performance, cost and fuel efficiency metrics. Because MechaCar is being marketed as a cost-effective sports-luxury car, we proposed to start by comparing cost to acceleration (0-60mph times). The null hypothesis (H0) is that there is no correlation between cost and acceleration. The alternative hypothesis (Ha) is that cost and acceleration do have a correlation. For the initial statistical test, we'd run a linear regression to visualize any obvious and /or significant correlation between cost and acceleration for all cars on the market this year. For this test, we'd need to have MSRP and mean 0-60 acceleration data for the cars in our analysis. To add to this analysis, we'd then calculate acceleration/cost ratios for all cars in the analysis and run a t-test to determine whether MechaCar's acceleration/cost ratio is significantly different from the mean acceleration/cost ratio for all cars in the study.

Beyond this initial analysis, we'd expect to perform some ANOVA testing of other performance metrics against vehicle class, transmission types and cost categories. ANOVA testing would be appropriate since it's suited to test the means of a single dependent variable across independent categorical variables with multiple groups.

