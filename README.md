# MechaCar Statistical Analysis

## Project Overview:

<b>

The upper management of a company named `AutosRUs` has approached their new employee `Jeremy` about a special project. The companies newest car prototype they call `MechaCar` is suffering from production troubles that are prohibiting the manufacturing teams's progress. We will help Jeremy and the data analytics team review the production data for insights that may help the manufacturing team. In this challenge, we will do the following below:

<br>

1. Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
2. Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
3. Run t-tests to determine if the manufacturing lots are statistically different from the mean population
4. Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.

<br>

## Linear Regression to Predict MPG

<br>

 

`Q1: Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?`

`Q2: Is the slope of the linear model considered to be zero? Why or why not?`

`Q3: Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?`

-    A1: Each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model. Vehicle length and ground clearance are statistically unlikely to provide random amounts of variance to the liner model. In other words, they are making a significant impact on mpg. 

-    A2: Examine the Pr(>|t|) value in the summary below for the (Intercept). The intercept is statistically significant (less than the 0.05) and not zero. This indicates that the intercept term explains a significant amount of variability in the dependent variable when all independent variables are equal to zero.

-    A3: The Multiple R-squared value of (.7149033) and a vary small p-value is indicative that this model does an adequate job of predicting mpg.

<p align=center>
<img src=Images/D1_linear_regres.png>

<br>

## Summary Statistics on Suspension Coils

<br>

`Q1: The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?`

-    A1: In total the specifications are met with a variance of 62.29 (less than 100).
-    A2: If we examine by each Lot, Lot 1 & 2 are within specifications; However, Lot 3 has a variance that exceeds the specifications of 100 PSI as outlined in the table below.
<br>

<p align=center>
<img src=Images/D2_total_summary.png width=695><img src=Images/lot_summary.png>

<br>

## T-Tests on Suspension Coils

<br>

`Run t-tests to determine if the manufacturing lots are statistically different from the population mean of 1500 PSI and evaluate the p-value for significance using a .05 level of significance.`

<br>

<p align=center>
<img src=Images/all_lots.png width= 920 height=320>

- **`Collectively, all lots` returned a p-value of `.06028` and are NOT significantly different from the population mean**

<p align=center>
<img src=Images/lot_1.png>

- **`Lot 1` is NOT significantly different from the population mean with a returned p-value of `1`**

<p align=center>
<img src=Images/lot_2.png>

- **`Lot 2` is NOT significantly different from the population mean with a returned p-value of `.6072`**

<p align=center>
<img src=Images/lot_3.png width=910>

- **`Lot 3` IS significantly different from the population mean with a returned p-value of `.04168`**

<br>

## Study Design: MechaCar vs Competition

When comparing MechaCar to its competition we should consider using an ANOVA test. An ANOVA test is a type of statistical test used to determine if there is a statistically significant difference between two or more categorical groups by testing for differences of means using variance.

Metric to be tested: Engine displacement (# of cylinders) and the affect on MPG.

Hypothesis: The more cylinders a vehicle has the lower MPG it will receive.

Statistical Test: A 4 cylinder, a 6 cylinder, and an 8 cylinder car were driven around on 10 gallons of gas in each of their tanks. They all drove the same exact route simultaneously. There was an even mixture of city and highway driving.

Data from Statistical Analysis: The results from the Statistical test confirmed the initial hypothesis. The 4 cylinder vehicle used the least amount of gas while the 8 cylinder used the most gas.

Using an ANOVA test we can compare the engine displacement and city/highway MPG of MechaCar's design and the competitors. If the p-value is greater than 0.05, then MechaCar has the same or similar performance in the category we are comparing them in. Alternatively, a p-value of 0.05 or lower is generally considered statistically significant. The lower the p-value that is returned, the greater the statistical significance of the observed difference.


<br>

## Summary:

By examining each Pr(>|t|) value which represents the probability that each coefficient contributes a random amount of variance to the linear model we can conclude that Vehicle length and ground clearance are statistically unlikely to provide random amounts of variance to the liner model. In other words, they are making a significant impact on mpg. The Multiple R-squared value of (.7149033) and a vary small p-value is indicative that this model does an adequate job of predicting mpg. Designers will need to consider these variables when continuing to design cars if their focus is based around fuel efficiency. Lot 3 is significantly different from the population mean with a returned p-value of (.04168).



## Resources:

- Software:

    - `RStudio`
    - `R`

<br>

- Resources:

    - `MechaCar_mpg.csv`
    - `Suspension_Coil.csv`
  
<br>

<b/>