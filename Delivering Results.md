# PyBer Analysis Report

## Background and Results

### Purpose
This assignment utilizes all the rideshare data from January to early May of 2019 to compare and contrast among three city types ("Rural", "Suburban" and "Urban") in number of rides, the number of drivers and total fares.  The summary will be used to improve access to ride-sharing services and determine affordability for underserved neighborhoods.

### Technical Analysis
The ride data and city data have been merged to form a new DataFrame and each columns have been grouped by the city types to provide total rides, driver counts and total fares for each type.  The Pandas and Matplotlib libraries were employed and the df.plot() function with the FiveThrityEight graph style was used to generate a multiline chart demostrating the total fare amount for each city type over the data time period.
https://github.com/hannahc1/PyBer_Analysis/blob/master/PyBer.ipynb

### Results
![](https://github.com/hannahc1/PyBer_Analysis/blob/master/Analysis/Table1.PNG)
The summary hightlights that Rural cities are in need of more drivers while the Urban cities seem to have excess number of drivers than the actual needs, hence bringing down the average fare per an Urban driver to 1/3 of an Rural driver.  The Rural cities may show significant growth in total fare when the size of the driver pool grows.  The summary indicates that the riders are used to and willing to pay $10 more per ride than the Urban riders.

![](https://github.com/hannahc1/PyBer_Analysis/blob/master/Analysis/Fig1.png)
![](https://github.com/hannahc1/PyBer_Analysis/blob/master/Analysis/Fig8.png)

### Summary
The summary DataFrame and the multiple-line graph both suggest that the Rural cities are currently underserved and there is a significant room to grow in total fare amount.


## Challenges Encountered and Overcome

### Challenges and Difficulties Encountered
When the ride data was merged with the city data, the total driver count for each city, instead of a unique driver ID for that perticular ride, was assigned to each ride.  A simple groupby() and sum() would not properly calculate the driver count for each city type.

### Technical Analyses Used
The driver count was calculated by using the following code:

![](https://github.com/hannahc1/PyBer_Analysis/blob/master/Analysis/Code1.PNG)
The means of each city was first calculated then the cities were grouped by city types to calculate the sum of the means.  The results would be the same if the original city data was grouped by the city types and the sums were calculated.

## Recommendations and Next Steps

### Recommendations for Future Analysis

### Additional Analysis 1

* Description of Approach
distance traveled,
* Technical Steps

### Additional Analysis 2
travel minutes and times
* Description of Approach

* Technical Steps
