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


**Get the number of students for 10th, 11th and 12th grade for Thomas High:** grade_10_to_12_thomas = school_data_complete_df.loc[((school_data_complete_df["school_name"] == "Thomas High School") & (school_data_complete_df["grade"] != "9th")), "student_name"].count()

Get the new percentage of students that passed math in Thomas High School:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/math_replace_9th.png)

**How does replacing the ninth-grade scores affect the following:**

- **Math and reading scores by grade**
The only scores that should change are the ones of the 9th grade of Thomas High School, the performance of the other schools is not affected by replacing the grades.

The example for the math and reading scores are as follows:
![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/Math_by_grade.png)
![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/Reading_by_grade.png)

To get the summary by grade, first it is necessary to create the series for each grade, group them by school name and then combine them into a DataFrame:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/Math_by_grade_DF.png)


- **Scores by school spending**

As expected, there is only change between the spending ranges of $586 to 630 and from $631 to $645:
![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/Scores_by_school_spending.png)

To get this result, we have to establish the bins, categorize them, calculate the averages for each field and then create the Data Frame:
![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/Scores_by_school_spending_DF.png)

- **Scores by school size**
In this category, there is no notable change:
![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/Scores_by_school_size.png)


- **Scores by school type**
There is also no notable change:
![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/Scores_by_school_type.png)

**Summary:** Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

- The main changes are the reading and math score of Thomas High School, the passing percentages (math, reading and overall). Also, it affects directly the performance of the school compared to the others, since it went from being the second best High School (according to overall passing percentage) to being the number 7.
