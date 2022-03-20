# School_District_Analysis
Data Bootcamp Module 4: PyCitySchools with Pandas
## Overview of Project

### The purpose of this project is to analyze the performance of a group of students and schools using Jupyter notebooks. At first, the results were obtained using the complete "students_complete.csv" and "schools_complete.csv" datasets, but after the first analysis some values of the student dataset were modified, as one grade of Thomas High School had invalid input (which changes the overall results of the analysis. By the end of this project, we are able to obtain and compare the following: 

* I. Summary of the district (and how is affected with the change of grades)
* II. Summary of each school (and how is affected with the change of grades)
* III. How the change of grades affects the High Schools were the changes were made
* IV. Effect of replacing grades in scores of each school (according to school spending, school size and school type)


## Resoruces
**For this analysis, the following resuorces were used**:
- Data Sources: students_complete.csv, schools_complete.csv
- Software: Jupyter Notebook 4.8

## Results

**Summary of the district (and how is affected with the change of grades)**

The comparison of the district summary, before and after the change of grades is as follows:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/District%20summary.png)

It is possible to see that the total amount of students and budget don't change, but the average scores on Math and Reading go down (as does the percent of students that passed).

To obtain the district summary, it is necessary to create a new Data frame, which is done with the following code:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/District_summary_DF.png)

**Summary of each school (and how is affected with the change of grades)**

First, the summary of schools before the change of grades:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/School_summary_before.png)

Then, the summary of schools after the change of grades:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/School_summary_after.png)

As we can see on both of the previous images, there is no change in 14 out of the 15 schools of the district, as the change of grades was made only on "Thomas High School" which really affected its performance.

To get the school summary first it is necessary to define each column using the original DataFrame and then create a new DataFrame that includes the columns previously defined. The script is as follows:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/School_summary_DF.png)

**How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?**

If one takes into consideration the grades of the 9 graders as "null", the replacing of grades has a huge effect on the Thomas High School Performance. It went from a 90.9% overall passing to only a 65%, which means that it went from being the second school overall to being the worst school over all.

Now, if one does not consider the 9th grade students, there is not much change on the performance of the school, it just went down 0.3% on the overall passing percent and maintained the #2 place. The top 5 schools (according to overall performance) are as follows:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/Top_5_not_9th_thomas.png)

To not consider the students of 9th grade for Thomas High School, we first have to obtain the number of students that are in 10th, 11th and 12th grade and then run back the analysis for that school but considering the new number of students instead of all the student. An example for the Math passing percentage is as follows:

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
