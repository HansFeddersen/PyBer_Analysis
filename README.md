# PyBer_Analysis

Data Bootcamp Module 5: PyBer with Matplotlib
## Overview of Project

### The purpose of this project is to analyze the data of a ride application in different cities. Each city has its own classification (Urban, Rural), a defined number of drivers and information of how many rides (and information for each ride) were done during a certain period of time. The main analysis is done by creating new DataFrames (to obtain and group the key information needed) and then by plotting it with the objective of having a visual understanding of the results.

## Resoruces
**For this analysis, the following resuorces were used**:
- Data Sources: city_data.csv, ride_data.csv
- Software: Jupyter Notebook 4.8
- Libraries: pandas, matplotlib.pyplot

## Process

To obtain the results showed below, the following process was done:

**Import libraries, load and read the csv files that are going to be used for the study:**

![This is an image](https://github.com/HansFeddersen/PyBer_Analysis/blob/main/Resources/More/libaries%2C%20load%20and%20read.png)

**Merge both DataFrames, by a common column (in this case "city")**

![This is an image](https://github.com/HansFeddersen/PyBer_Analysis/blob/main/Resources/More/Merge%20DF.png)

**Get a Summary DataFrame**
To get a Summary DataFrame, we need to work with the information to get calculate the fields that we want to have on our summary In this case we are going to analyze the information of the rides for each city type (Urban, SubUrban and Rural) so it is neccesary to group by "type".

The fields included on the summary are the following:
- **Total rides per city type:** Count how many rides are per each city type
- **Drivers per city type:** Add the number of drivers for each city type
- **Total amount of fares per city type):** Add all the fares for each city (grouped by city type)
- **Average fare per ride for each city type:** All of the fares per city type, divided by the total amount of rides per city type
- **Average fare per rider for each city type:** All of the fares per city type, divided by the total amount of drivers per city type.

Finally, we create a new DataFrame with the information of our summary, and the summary is as follows:

![This is an image](https://github.com/HansFeddersen/PyBer_Analysis/blob/main/Resources/More/Summary_DF.png)

With this summary is easier to understand the information per city, but it can be even more clear and complete if we create a line graph showing how the total amount of fares for each city behaves in time, for that we have to do the following:

- **Create a new data frame (from the original merge) grouping by date and city time:** We add all the fares for the same Date and time and City type:

![This is an image](https://github.com/HansFeddersen/PyBer_Analysis/blob/main/Resources/More/New_date_and_type_DF.png)

- **Create a pivot table with the date as the index and then filter the desired dates using the function loc:**
![This is an image](https://github.com/HansFeddersen/PyBer_Analysis/blob/main/Resources/More/Pivot_table.png)

As we can see on the pivot table, there are many empty or "NaN" values, so we group the dates by week (using the resample function) to avoid this:

![This is an image](https://github.com/HansFeddersen/PyBer_Analysis/blob/main/Resources/More/Resample_pivot.png)




