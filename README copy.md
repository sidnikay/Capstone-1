# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Problem Statement

Many students aim for admission to a prestigious college or university, but what are their chances of admittance? This project aims to determine the correlation between between the top ranked schools, test scores, and  acceptance. 

---
### Background Research & Sources

I am working from the perspective of a guidance counselor. The 25 top ranked schools contain the 8 Ivy-league college and universities and 17 other very well known schools, such as MIT. I researched the efficacy of having a prestigious school degree. Whether having a degree from such a school, increases a persons ability to have a successful career and life. It is safe to say having a degree does increase ones happiness in life, simple due to higher rates of employment and increased salaries. However, where the degree is obtained matters less. According to INC., people who had close relationships with their parents are often the people to do their best in life. I used the SAT and ACT scores to help me determine what a students scores would need to be to get into a prestigious school. As a guidance counselor, it is my job to provide students and parents, with all the tools they need to determine what is best for them. 


---
### Datasets Used

* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* [`sat_act_by_college.csv`](./data/sat_act_by_college.csv): Ranges of Accepted ACT & SAT Student Scores by Colleges ([source](https://www.compassprep.com/college-profiles/))

---

### Data Dictionary=
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|act_2019|The states involved in the ACT.| 
|**act participation**|*float*|act_2019|The participation percentage rate of states who took the ACT expressed by decimal.|
|**act test scores**|*float*|act_2019|The states average of ACT scores.|
|**state**|*object*|sat_2019|The states involved in the SAT.|
|**sat participation**|*float*|sat_2019|The participation percentage rate of states who took the SAT expressed by decimal.|
|**sat test scores**|*int*|sat_2019|The states average of SAT scores.|
|**school**|*object*|sat_act_by_college|the name of each college or university.|
|**test required**|*object*|sat_act_by_college|Yes or NO requirement of the SAT or ACT.|
|**number of applicants**|*int*|sat_act_by_college|Th number of students who applied for the school year.|
|**acceptance rate**|*float*|sat_act_by_college|The percentage of students accepted to school expressed by decimal.|
|**sat admission scores (25th-75th)**|*object*|sat_act_by_college|The 25th-75th percentile range of SAT scores accepted by each school.|
|**act admission scores (25th-75th)**|*object*|sat_act_by_college|The 25th-75th percentile range of ACT scores accepted by each school.|
|**median sat scores**|*float*|sat_act_by_college|The median SAT score expected by the school based off the SAT admission scores (25th-75th).|
|**median act scores**|*float*|sat_act_by_college|The median ACT score expected by the school ACT admission scores (25th-75th).|
|**approximate students accepted**|*float*|sat_act_by_college|The number of students applied divided by the school acceptance rate.|
---

### Analysis Summary

I started by importing the DataFrames for 2019 SAT Scores and 2019 ACT Scores from 2019, and the SAT and ACT Scores by college. From there, I cleaned the data from erroneous and missing data. I merged the SAT and ACT 2019 Scores to get better comparison against the SAT and ACT Scores by college.

I found nations average test results for the SAT and ACT in 2019.
![Figure A](https://git.generalassemb.ly/sidnikay/Submissions/blob/master/projects/project_1-master/images/Nations%20average%20SAT%20and%20ACT%20Test%20Scores.png)

I found the rate of acceptance based off the median SAT or ACT scores accepted by top ranked schools. 
![Figure B](https://git.generalassemb.ly/sidnikay/Submissions/blob/master/projects/project_1-master/images/Number%20of%20applicants%20vs.%20axp.%20students%20accepted%20%20by%20schools.png)

I evaluated the relationship between number of applicants and the acceptance rate. 
![Figure C](https://git.generalassemb.ly/sidnikay/Submissions/blob/master/projects/project_1-master/images/acceptance%20rate%20and%20median%20SAT%20and%20ACT%20score.png)

I evaluated the relationship between number of applicants and the approximate number of students accepted by schools.
![Figure D](https://git.generalassemb.ly/sidnikay/Submissions/blob/master/projects/project_1-master/images/acceptance%20rate%20vs.%20number%20of%20applicants.png)

I found students with the highest scores in SAT or ACT, when applying to the top ranked schools, have a narrow chance of getting accepted to 1 school. 

---

### Conclusions & Considerations

In the wake of actresses Lori Loughlin and Felicity Huffman college scandal, parents should help their child decide whether the competition for top ranked school is worth it. As a guidance counselor, I see the stress of applying for a prestigious school. However, I am here to support the parents and students to the best of my ability. I would recommend that my student apply to several top ranked schools to increase the likely hood of admittance. I would guide them to try and get an SAT score between (1440-1570) and ACT score between (32-35). I would also look into what other criteria these top ranked schools are looking for in their applicants, to increase the students chances of getting in.

---

### Sources Cited:
*[Top Ranked Schools]https://blog.spiveyconsulting.com/2020-us-news-undergraduate-rankings/

*[Average ACT Scores]https://magoosh.com/hs/act/2019/act-scores/

*[Average SAT Scores]https://www.cappex.com/articles/testing/what-is-a-good-SAT-score

*[Ivy League Schools]https://en.wikipedia.org/wiki/Ivy_League

*[University of Utah's SAT Score Range]https://www.prepscholar.com/sat/s/colleges/University-of-Utah-admission-requirements