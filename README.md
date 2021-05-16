# School_District_Analysis

### Resources
- Software: Python 3.7.6, Jupyter Notebook, Anaconda
- CSV files with data are in the [Resources](https://github.com/adampaseltiner/School_District_Analysis/tree/main/Resources) folder
- Due to DataFrame display issues in GitHub this analysis can also be viewed in [Jupyter Notebook Viewer](https://nbviewer.jupyter.org/github/adampaseltiner/School_District_Analysis/blob/main/PyCitySchools_Challenge.ipynb)

## Overview
For this project we analyzed data for Maria's school district to help inform her of their performance by correlating data fields such as school funding, school size, school type, and student grades. After performing our initial analysis, however, we were notified of potentially fraudulent grades submitted by 9th grade students at Thomas High School and were asked to perform the analysis again to account for the bad data. 

## Results

The first comprehensive run through the data analysis utilized the full student data set and yielded detailed results about Maria's school district. Once we received notice of the supposedly dishonest 9th grade students at Thomas High School, we needed to go back and perform our analysis again to remove their grades from the data set in hopes of getting a more accurate picture of the true statistics for the school district. 

To remove these grades we began by replacing all Thomas High School's 9th grader's scores with NaN:

![NaNs](https://user-images.githubusercontent.com/82347825/118382059-4838e000-b5bf-11eb-9b71-3110caac7aa3.png)

Once we replaced an entire school's grades worth of scores, we saw the change had an affect on several factors in our analysis.

---

Filling in the 9th graders scores with NaN resulted in the following changes:
- For the district summary: the before and after shows the overall passing percentages stay nearly the same with only tenths of a percentage difference:

![district_summary_before](https://user-images.githubusercontent.com/82347825/118382142-71a63b80-b5c0-11eb-837b-3e06ec75ba3b.png)

![district_summary_after](https://user-images.githubusercontent.com/82347825/118382996-2859ea00-b5c8-11eb-8a9e-61803ba94975.png)

- For the school summary, we see a much larger impact since Thomas High School's passing %'s all dropped dramatically:

![Thomas_before](https://user-images.githubusercontent.com/82347825/118383419-6b698c80-b5cb-11eb-8cc8-786abe714c52.png)
  
![Thomas_after](https://user-images.githubusercontent.com/82347825/118383421-6d335000-b5cb-11eb-8386-27fc6571b7aa.png)

- Changing the 9th graders scores moved Thomas High School out of the top 5 in Percentage Overall Passing to one of the lowest. However, once those scores were omitted from the calculation Thomas High School remained one of the top performing high schools.

![Top5PostOmission](https://user-images.githubusercontent.com/82347825/118384105-79baa700-b5d1-11eb-865b-8e0c6141aca1.png)

Further observations from the ninth-grade score replacement:
- Math and reading scores by grade remained the same for all other grades, with the ninth-grade being replaced by NaN

![Scores_by_grade](https://user-images.githubusercontent.com/82347825/118384353-71fc0200-b5d3-11eb-89d6-67a8ca7150de.png)

- Scores by school spending did not change, with schools spending small to medium budgets per student performing the best

![Spending](https://user-images.githubusercontent.com/82347825/118384449-08c8be80-b5d4-11eb-839d-c0c7a8ea57bb.png)

- School that were small to medium in size performed significantly better than the larger schools

![Size](https://user-images.githubusercontent.com/82347825/118384482-4fb6b400-b5d4-11eb-9bab-7232f86cd5f0.png)

- Charter schools significantly outperform district schools

![Type](https://user-images.githubusercontent.com/82347825/118384511-82f94300-b5d4-11eb-8ef6-ebe24944888c.png)

## Summary
  - Average Math Score dropped from 79% to 78.9%
  - Percent Passing Math dropped from 75% to 74.8%
  - Percent Passing Reading dropped from 86% to 85.7%
  - Percent Overall Passing dropped from 65% to 64.0%

