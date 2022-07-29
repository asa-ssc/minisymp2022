---
layout: page-fullwidth
title: "Data Jamboree"
header: no
permalink: /jamboree/
---

The data jamboree is a party of computing tools for solving the same data science
problem. The main data set is the NYC motor vehicle collisions data. The
real-time full data with documentation is available from 
[NYC Open
Data](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95).
Here we only consider a subset which contains the crashes in [January,
2022](https://github.com/statds/ids-s22/raw/main/notes/data/nyc_mv_collisions_202201.csv).
This dataset contains a column of zip code for each crash.


There are 178 unique zip codes in this subset data.
The median household income at the zip code level from the American Community
Survey can be obtained from the
[census with appropriate
filters](https://data.census.gov/cedsci/table?t=Income%20%28Households,%20Families,%20Individuals%29&g=0400000US36%248600000&y=2020&tid=ACSST5Y2020.S1903). 
We downloaded the [income data for all the zip codes in the NY
State from the 2020 American Community
Survey](https://github.com/statds/ids-s22/raw/main/notes/data/ACSST5Y2020.S1903_2022-07-29T145042.zip).
The column `S1903_C03_015E` contains the median income of all 1794 zip codes in
the NY State.
The zip code level crash data of NYC can be merged with the median hoursehold
income when zip code level analyses are of  interest. The zip code boundaries of
NYC can be downloaded from [NYC open
data](https://data.cityofnewyork.us/Business/Zip-Code-Boundaries/i8iw-xf4u).


The scientific exercises of the jamboree are:
+ Create a frequency table of the number of crashes by borough.
+ Create an `hour` variable with integer values from 0 to 23, and plot of the
  histogram of crashes by hour.
+ Check if the number of persons killed is the summation of the number of
  pedestrians killed, cyclist killed, and motorists killed. From now on, use the
  number of persons killed as the sum of the pedestrians, cyclists, and
  motorists killed.
+ Construct a cross table for the number of persons killed by the contributing
  factors of vehicle one. Collapse the contributing factors with a count of less
  than 100 to “other”. Is there any association between the contributing factors
  and the number of persons killed?
+ Create a new variable death which is one if the number of persons killed is 1
  or more; and zero otherwise. Construct a cross table for death versus
  borough. Test the null hypothesis that the two variables are not associated.
+ Visualize the crashes.
+ Fit a logistic model with death as the outcome variable and covariates that
  are available in the data or can be engineered from the data. Example
  covariates are crash hour, borough, number of vehicles involved,
  etc. Interprete your results.
+ Aggregate the data to the zip-code level and connect with the census data at
  the zip-code level.
+ Visualize and model the count of crashes at the zip-code level.

