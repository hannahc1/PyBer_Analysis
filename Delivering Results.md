# PyBer Analysis Report

## Background and Results

### Purpose
   This assignment utilizes all the rideshare data from January to early May of 2019 to compare and contrast among three city types ("Rural", "Suburban" and "Urban") in the number of rides, the number of drivers and the total fares.  The summary will be used to improve access to ride-sharing services and determine affordability for underserved neighborhoods.

### Technical Analysis
   The ride data and city data have been merged to form a new DataFrame and each columns have been grouped by the city types to calculate the total rides(count()), driver counts (mean() & groupby()) and total fares (sum()) for each city type.  The Pandas and Matplotlib libraries were imported and the df.plot() function with the FiveThrityEight graph style was used to generate a multiple-line graph demostrating the total fare amount for each city type over the data time period.
https://github.com/hannahc1/PyBer_Analysis/blob/master/PyBer.ipynb

### Results
![](https://github.com/hannahc1/PyBer_Analysis/blob/master/Analysis/Table1.PNG)

   The summary above suggests that the Rural cities are in need of drivers while the Urban cities seem to have excess number of drivers than the actual needs, hence bringing down the average fare per an Urban driver to 1/3 of an Rural driver.  The below bubble chart below illustrates how the number of rides and fare are related to the average number of the drivers for each city type.  The fewer drivers and the fewer rides there are, the higher fare each ride costs.

![](https://github.com/hannahc1/PyBer_Analysis/blob/master/Analysis/Fig1.png)

   The multiple-line graph below demonstrates the total fares per week for the Urban cities are 5x of that for the Rural cities and the total fares disparity is pretty constant week over week.

![](https://github.com/hannahc1/PyBer_Analysis/blob/master/Analysis/Fig8.png)

### Summary
   The summary DataFrame and the multiple-line graph both suggest that the Rural cities are currently underserved and there is a significant room to grow in total fare amount.


## Challenges Encountered and Overcome

### Challenges and Difficulties Encountered
   When the ride data was merged with the city data, the total driver count for each city, instead of a unique driver ID for that perticular ride, was assigned to each ride.  A simple groupby() and sum() would not properly calculate the driver count for each city type.

### Technical Analyses Used
   The driver count was calculated by using the following code:
![](https://github.com/hannahc1/PyBer_Analysis/blob/master/Analysis/Code1.PNG)

   The means of each city was first calculated then the cities were grouped by city types to calculate the sum of the means.  The results would be the same if the original city data (pre-merging) was grouped by the city types and the sums were calculated.

## Recommendations and Next Steps

   The summary indicates that the Rural riders are used to, and probably willing to pay $10 more per ride than the Urban riders.  The Rural cities may experience significant growth in total fares if more rides become available by increasing the number of drivers in the Rural cities.

### Recommendations for Future Analysis

### Additional Analysis 1

* Description of Approach:
---
Number of rides per week for each city type.

* Technical Steps
1. Calculate the sum() of rides by the type of city and date using groupby() to create a Series.
2. Convert the groupby Series into a DataFrame.
3. Reset the index and create a pivot talbe DataFrame with the Date as the index and columns = 'City Type'.

### Additional Analysis 2

* Description of Approach:
---
Average area for each city types (to approximate the length of the ride) and average fare per square mile for each city type.

* Technical Steps
1. Add the "area" column to the city data and fill the values with the area data for each city.
2. Combine the city data with the ride data.
3. Get the sum of the area for each city by each city type using groupby(["type","city"]).mean()["area"].groupby(["type"]).sum().
4. Get the average area by dividing the sum of the city counts for each city type.
5. Get the average fare per square mile by dividing the average fare by the average area.
6. Add two columns to the summary DataFrame.
