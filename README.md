# School_District_Analysis
Data Bootcamp Module 3: PyCitySchools with Pandas
## Overview of Project

### The purpose of this project is to anlalyze the performance of a group of students and schools using Jupyter notebooks. At first, the results were obtained using the complete "students_complete.csv" and "schools_complete.csv" datasets, but after the first analysis some values of the student dataset were modified, as one grade of Thomas High School had invalid input (which changes the overall results of the analysis. By the end of this project, we are able to obtain and compare the following:
* I. Summary of the disctrict (and how is affected with the change of grades)
* II. Summary of each school (and how is affected with the change of grades)
* III. How he change of grades affect the High Schools were the changes were made
* IV. Effect of replacing grades in scores of each school (according to school spending, school size and school type)


## Resoruces
**For this analysis, the following resuorces were used**:
- Data Sources: students_complete.csv, schools_complete.csv
- Software: Jupyter Notebook 4.8

## Results

**Summary of the disctrict (and how is affected with the change of grades)**

The comparison of the district summary, before and after the change of grades is as follows:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/District%20summary.png)

It is possible to see that the total amount of students and budget don't change, but the average scores on Math and Reading go down (as does the percent of students that passed).

To obtain the district summary, it is necessary to create a new Data frame, which is done with the following code:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/District_summary_DF.png)

**Summary of each school (and how is affected with the change of grades)**

First, the summary o schools before the change of grades:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/School_summary_before.png)

Then, the summary of schools after the change of grades:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/School_summary_after.png)

As we can see on both of the previous images, there is no change in 14 out of the 15 schools of the district, as the change of grades was made only on "Thomas High School" which really affected its performance.

To get the school summary first it is necessary to define each column using the original DataFrame and then create a new DataFrame that includes the columns previously defined. The script is as follows:

![This is an image](https://github.com/HansFeddersen/School_District_Analysis/blob/main/Resources/More/School_summary_DF.png)

**County with the largest number of votes**

The county with the largest number of votes was Denver. There were 306,055 casted votes in Denver (82,8% of the total) and of those votes 239,282 were fo candidate Diana DeGette (72.8%), 57,188 were for candidate Charles Casper Stockham (18,7%) and 9,585 were for candidate Raymon Anthony Doane (3.1%).

The script to get this result is as follows:

![This is an image](https://github.com/HansFeddersen/Election_Analysis/blob/main/Challenge/Resources/More/largest_county.png)

**Breakdown of the number of votes and the percentage of the total votes each candidate recieved**

The candidate with the most votes on her/his favor was Diana Degette with 272,892 votes (73.8%), followed by Charles Casper Stockham with 85,213 votes (23%) and finally Raymon Anthony Doane with 11,686 votes (3.1%).

The script to get this result is as follows:

![This is an image](https://github.com/HansFeddersen/Election_Analysis/blob/main/Challenge/Resources/More/Votes_per_candidate.png)

**Candidate that won the election, his/her vote count and percentage of the total votes**

The election was won by Diana Degette with 272,892 votes on her favor, which represents a 73,8% of the total votes. All the votes that she obtained on Denver were sufficient to win the election (due to difference of casted votes between Denver and the other two counties).

The script to get this result is as follows:

![This is an image](https://github.com/HansFeddersen/Election_Analysis/blob/main/Challenge/Resources/More/Winning_candidate.png)

## Election-Audit Summary

- The script is written to work with any election data that follows the same format as the election_results.csv used (Ballot Id, County and Candidate). The script can be modified to print more results about these elections. Results such as, candidate outcome on each county or group of two counties.

**Also, the script can be modified for other elections that have different data structures. Examples are as follows:**

- Elections for city/state/country position (such as senator or president) where you can group the information by county, city and state. For this analysis the code should be modified to contain more dictionaries with all the counties that belong to one city and all the cities that belong to one state. Then one gets and group the results to have a very delicate analysis of the elections.

- Elections such as the US presidential election where the candidate that wins the popular vote, does not necessarily wins the election (because each state represents a certain number of electors from the electoral college). One can introduce the data of how many electors does each state give and get the outcome of how many electoral votes each of the candidates received.
