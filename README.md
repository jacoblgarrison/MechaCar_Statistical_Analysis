# MechaCar_Statistical_Analysis

Using R to analyze why AutosRUs is having production issues with its' MechaCar. 

## Overview

AutosRUs wants to utilize R to see why the MechaCar is having issues during the production stage. We will use a few methods to analyze why the car is having any problems. Those methods will include linear regression, producing a summary statistics table to analyze results, and a t-test to determine if manufacturing lots and each individual lot are statistically different than the population mean of 1,500 pounds per square inch.

## Results

## Linear Regression to Predict MPG 

![Deliverable 1 Linear Regression Model](https://user-images.githubusercontent.com/95515322/163737019-c01ed8ce-0042-4656-9ced-9b10740cb6c9.png)

The variables that provide a non-random amount of variance to the mpg value in the dataset would be **vehicle_length** and **ground_clearance.** The variable vehicle_length has a p-value of 2.60x10^-12, which is well below the typical significance value of .05. With a p-value this low, we can be assured that this is a non-random amount of variance to the mpg values. The ground_clearance variable also has an extremely low p-value of 5.21x10^-8 which is also well below the typical significance value of .05. We can safely say that both of these variables contribute a non-random amount of variance to the mpg values. 

The slop of the linear model is not considered to be zero. With a p-value of 5.35x10^-11, this is extremely low and below a value of .05. This means we would reject the null hypothesis.

This model does help us predict the mpg of our MechaCar, with an r-squared value of 0.7149, we can round up and say the model is 72% accurate. There is room to improve but we can acknowledge it is beneficial.

## Summary Statistics on Suspension Coils

![total_summary](https://user-images.githubusercontent.com/95515322/163737481-bd2ec4c5-c1c2-4b42-b7fa-9d56f4beb834.png)

![lot_summary](https://user-images.githubusercontent.com/95515322/163737531-5760cec0-86de-4462-b405-774a330a9a39.png)

As we can see in the tables above, our total summary shows us a variance under 100 pound per square inch with a value of 62.29. However when we look at our lot summary table, lots 1 & 2 appear to be fine, yet lot 3 has a variance of 170 which is well above our threshold. 

## T-tests on Supsension Coils

![One Sample t-test Suspension_Coil_df$PSI](https://user-images.githubusercontent.com/95515322/163741760-2c8399de-bbd7-4870-a719-96e26f752c70.png)

The t-test for all of the manufacturing lots is shown above, and from this we can fail to reject the null hypothesis since the p-value is .06028, which is above a significance value of .05. We can determine it is not statistically different than the population mean. 

![One Sample t-test Suspension_Coil and Manufacturing Lot A](https://user-images.githubusercontent.com/95515322/163741872-47901d21-db41-4e75-aa18-fd9af9fad3e9.png)

The p-value for Lot 1 is shown to be 1, which is not low enough to be statistically different than the population mean. We fail to reject the null hypothesis. 

![One Sample t-test Suspension_Coil and Manufacturing Lot B](https://user-images.githubusercontent.com/95515322/163742041-8ff01261-da1f-4da6-af1b-e6510c373eb1.png)

Our p-value for lot 2 is .6072, which is not lower than .05. We fail to reject the null hypothesis. 

![One Sample t-test Suspension_Coil and Manufacturing Lot C](https://user-images.githubusercontent.com/95515322/163742101-b23f92e0-af69-47ad-a737-3e046deb1d8d.png)

Our p-value for Lot 3 is .04168, which is below the signifiance level of .05. We reject the null hypothesis and our statistics show this is different than the population mean. 

## Study Design: MechaCar vs. Competition

One of the key factors when thinking of which car to purchase is if the car you are buying will be reliable. To measure reliability, let's look at the maintenance cost of our MechaCar vs the competition. 

### Metric to Test

Let's look at the dollars ($USD) spent to maintain our MechaCar in comparison to the competition.

### Null and Alternative Hypothesis

Null Hypothesis: MechaCar's average maintenance cost in $USD is similar to competitor's vehicles. 
Alternative Hypothesis: MechaCar's average maintenance cost in $USD is statistically above or below that of competitor vehicles.

### What Statistical Test Would We Use?

We would use a two sample t-test.

### What Data Is Needed?

We would examine dollars spent on our MechaCar over a 7 year period and compare it to the dollars spent on our competitor's vehicle in the same class over a 7 year period.
