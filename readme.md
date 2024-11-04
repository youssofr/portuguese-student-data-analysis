# Student Scores
## Project Description

In this data analysis learning project I have worked dataset is of student achievement in secondary education of two Portuguese schools. The dataset is available on kaggle from this link. The data is originally from Paulo Cortez, University of Minho, and available on this link. 

I have performed through exploratory analysis on the data in order to find useful insight and interesting correlations between different factors.

I have then using the findings from the exploratory data analysis created a presentation section where the main findings are presented clearly in polished visuals.

##  Dataset Description

The data includes demographic information about students (such as gender, age, and adress), social information (such as number of family members, parents status, together or apart, romantic relationship of student, in a relationship or not) as well as some information about personal habits (such as how much free time do they have, how much time do they study, and how frequently do they go out), and most importantly academic information about the students, the academic information comprises of the grades in the Portuguese language over three academic periods, and one other feature; the number of absence days of students over the period of the study. </br>

The features mentioned were collected by using school reports and questionnaires. The data is intended to be used in machine learning appluications to predict the grade of the third period given knowledge of the rest of the demographic, social, and personal features in the data, as well as the grades of the students in the first two periods. </br>

I found this dataset very interesting to investigate as we can not only use it in its intended context, but we also can learn more about different non-academic factors which might affect students performance so we can ultimately suggest how we can enhance students well being and performance. </br>

All features in the dataset:


| Variable   |                              Description                                        |  Variable Taxonomy (Type) |
| -----------| ------------------------------------------------------------------------------- |---------------------------|
| school     | student's school (binary: 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)| Categorical - Nominal     |
| sex        | student's sex (binary: 'F' - female or 'M' - male) | Categorical - Nominal |
| age        | student's age (numeric: from 15 to 22) | Quantitave- Discrete - Ratio     |
| address    | student's home address type (binary: 'U' - urban or 'R' - rural) | Categorical - Nominal     |
| famsize    | family size (binary: 'LE3' - less or equal to 3 or 'GT3' - greater than 3) | Categorical - Ordinal     |
| Pstatus    | parent's cohabitation status (binary: 'T' - living together or 'A' - apart) | Categorical - Nominal     |
| Medu       | mother's education (numeric: 0 - none, 1 - primary education (4th grade), 2 - 5th to 9th grade, 3 - secondary education or 4 - higher education) | Categorical - Ordinal     |
| Fedu       | father's education (numeric: 0 - none, 1 - primary education (4th grade), 2 - 5th to 9th grade, 3 - secondary education or 4 - higher education) | Categorical - Ordinal     |
| Mjob       | mother's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other') | Categorical - Nominal     |
| Fjob       | father's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other') | Categorical - Nominal     |
| reason     | reason to choose this school (nominal: close to 'home', school 'reputation', 'course' preference or 'other') | Categorical - Nominal     |
| guardian   | student's guardian (nominal: 'mother', 'father' or 'other') | Categorical - Nominal     |
| traveltime | home to school travel time (numeric: 1 - <15 min., 2 - 15 to 30 min., 3 - 30 min. to 1 hour, or 4 - >1 hour) | Categorical - Ordinal     |
| studytime  | weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours, 3 - 5 to 10 hours, or 4 - >10 hours) | Categorical - Ordinal     |
| failures   | number of past class failures (numeric: n if 1<=n<3, else 4) | Categorical - Ordinal     |
| schoolsup  | extra educational support (binary: yes or no) | Categorical - Nominal     |
| famsup     | family educational support (binary: yes or no) | Categorical - Nominal     |
| paid       | extra paid classes within the course subject (Math or Portuguese) (binary: yes or no) | Categorical - Nominal     |
| activities | extra-curricular activities (binary: yes or no) | Categorical - Nominal     |
| nursery    | attended nursery school (binary: yes or no) | Categorical - Nominal     |
| higher     | wants to take higher education (binary: yes or no) | Categorical - Nominal     |
| internet   | Internet access at home (binary: yes or no) | Categorical - Nominal     |
| romantic   | with a romantic relationship (binary: yes or no) | Categorical - Nominal     |
| famrel     | quality of family relationships (numeric: from 1 - very bad to 5 - excellent) | Categorical - Ordinal     |
| freetime   | free time after school (numeric: from 1 - very low to 5 - very high) | Categorical - Ordinal     |
| goout      | going out with friends (numeric: from 1 - very low to 5 - very high) | Categorical - Ordinal     |
| Dalc       | workday alcohol consumption (numeric: from 1 - very low to 5 - very high) | Categorical - Ordinal     |
| Walc       | weekend alcohol consumption (numeric: from 1 - very low to 5 - very high) | Categorical - Ordinal     |
| health     | current health status (numeric: from 1 - very bad to 5 - very good) | Categorical - Ordinal     |
| absences   | number of school absences (numeric: from 0 to 93) | Quantitave- Discrete - Ratio     |
| G1         | first period grade (numeric: from 0 to 20) | Quantitave- Discrete - Ratio     |
| G2         | second period grade (numeric: from 0 to 20) | Quantitave- Discrete - Ratio     |
| G3         | final grade (numeric: from 0 to 20, output target) | Quantitave- Discrete - Ratio     |

## Summary of Findings
From the exploratory analysis I have found out that  all the following features show some effect on the students' grades. (when I say shows some effect this means that the median, and the five number summaries of each level of this variable eaither increase or decrease systematically in as we move in one direction, in the case of ordinal variables, or from level to the other, in the case of nominal varaibels.)

These Variables are:

1. __School:__ there is a significant difference between the scores of students from the two schools.
2. __Sex:__ Female students have higher scores distribution than male students.
3. __Address:__ Students in one location have lower score distribution than the other. (this might be because of travel time)
4. __Mother Education:__ The higher the mother's educaitonal level the higher the scores.
5. __Father Education:__ The higher the father's educaitonal level the higher the scores.
6. __Mother Job:__ Children of teacher have significantly higher grades than the rest of the students.
7. __Father Job:__ Children of teacher have significantly higher grades than the rest of the students.
8. __Travel Time:__ The longer the travel time the lower the score distribution.
9. __Study Time:__ The higher the study time the higher the score distribution (very expectedly so :"D). Yet the last two levels of study time don't have much differences.
10. __Activities:__ Students who participate in activities have on average higher grades.
11. __Higher Education:__ Students who want to pursue higher education have on average much higher grades.
12. __Internet:__ Students with internet access have on average higher grades.
13. __Family Relations:__ Students with better family relations have better grades.
14. __Go Out:__ Students who are in the second level, next to least, have the highest grades. And from there, there is a systematic decrease in grades when going out is more frequent.
15. __Daiy Alchohol use:__ The higher the consumption the lower the grades.

If we are to make a machine learning model, I would recommend that these variable be assigned higher weights in prediction or be the only ones to be used. But for the porpuses of our analysis, finding the factors which can effect the students performance, we have different considerations and not all factors can be treated as useful.

Firstly, there are the factors which only present can not, with only the information available to us in this study, be generalized to give any conclusions about education quality in general. These variables are:

1. __School.__
2. __Address.__
3. __Sex.__

Secondly there are social factors which affect the students grades. Those are:

1. __Mother And Father Education.__
2. __Mother And Father Jobs.__
3. __Family Relations.__


The rest of the factors can be reasonably be in the control of the students. These variables are:

1. __Travel Time.__
2. __Study Time.__
3. __Activities__
4. __Higher Education__
5. __Go Out.__
6. __Daily Alchohol Use.__


## Key insights for presentation

The presentation I would like to make is for the students. The messages which I can deliver based on studying this dataset (although it is not statistically verified to be signifcant, which we need to do, but this is the scope of our study for now) -- the messages are:

1. Study more. Very obviously :"D if you study more you are gonna get better results.
2. Go to a school neer your home. The higher the travel time the less your performance is expected to be.
3. Aim high. Having a goal for your study will likely affect your performance positively.
4. Balance your time between studying and going out and doing other activities. This point is very interesting for investigation in the multivariate section, in order to learn what combinations are best.
5. Limit your use of alchohol on week days. Students who use alchohol more on week days perform more poorly.
