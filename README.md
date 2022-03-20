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

**How many votes were casted in this congretional election?**

According to the results of the eletion, a total of 369,711 votes were casted.

The script to get this result is as follows (total votes started from 0):

![This is an image](https://github.com/HansFeddersen/Election_Analysis/blob/main/Challenge/Resources/More/Total%20_number%20_of_votes.png)

**Breakdown of the number of votes and the percentage of votes for each county in the precint**

Of the 369,711 casted votes, the county with the largest number of votes was Denver with 306,055 votes (82.8%), followed by Jefferson with 38,855 votes (10,5%) and in the last place Arapahoe with 24,801 votes (6.7%).

The script to get this result is as follows:

![This is an image](https://github.com/HansFeddersen/Election_Analysis/blob/main/Challenge/Resources/More/Votes_per_county.png)
![This is an image](https://github.com/HansFeddersen/Election_Analysis/blob/main/Challenge/Resources/More/Percntage_per_county.png)


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
