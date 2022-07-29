---
layout: page-fullwidth
title: "Data Jamboree"
header: no
permalink: /jamboree/
---

The data jamoree is a party of computing tools for solving the same data science
problem. The main data set is the NYC motor vehicle collisions data. The
real-time full data with documentation is available from 
[NYC Open
Data](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95).
Here we only consider a subset which contains the crashes in [January,
2022](https://github.com/statds/ids-s22/raw/main/notes/data/nyc_mv_collisions_202201.csv).

Since the data contains a column of zip code, we can get zip-code level data
from the census. ....

For visualization, the zip code boundaries of NYC can be found at
<https://data.cityofnewyork.us/Business/Zip-Code-Boundaries/i8iw-xf4u>.

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
+ Visualize the crashes, possibly by animation.
+ Fit a logistic model with death as the outcome variable and covariates that
  are available in the data or can be engineered from the data. Example
  covariates are crash hour, borough, number of vehicles involved,
  etc. Interprete your results.
+ Aggregate the data to the zip-code level and connect with the census data at
  the zip-code level.
+ Visualize and model the count of crashes at the zip-code level.

