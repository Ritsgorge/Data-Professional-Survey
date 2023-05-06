# Introduction
According to the definitions adopted by the EU, data professionals are workers who collect, store, manage, analyse and interpret findings for actionable insights. Skilled data experts are some of the most in-demand professionals in the world. These ranges from data engineers to data analysts as well as data architects and data scientists among a host of other titles. With an increasing demand for data professionals, most often the supply of professionals seem to be inversely proportional. 

# About dataset
This is an online questionnaire designed for data professionals to provide data pertaining to their roles based on specific questions. I downloaded the dataset from the more section of AlexTheAnalyst youtube video tutorial on PowerBI. The dataset is a csv file containing 17,668 rows and 28 columns. The columns include; Unique ID	Email, Date Taken (America/New_York), Time Taken (America/New_York), Browser, City, OS,	Country, Referrer, Time Spent, Q1 - Which Title Best Fits your Current Role?, Q2 - Did you switch careers into Data?, Q3 - Current Yearly Salary (in USD), Q4 - What Industry do you work in?, Q5 - Favorite Programming Language, Q6 - How Happy are you in your Current Position with the following? (Salary), Q6 - How Happy are you in your Current Position with the following? (Work/Life Balance), Q6 - How Happy are you in your Current Position with the following? (Coworkers), Q6 - How Happy are you in your Current Position with the following? (Management), Q6 - How Happy are you in your Current Position with the following? (Upward Mobility), Q6 - How Happy are you in your Current Position with the following? (Learning New Things), Q7 - How difficult was it for you to break into Data?, Q8 - If you were to look for a new job today, what would be the most important thing to you?, Q9 - Male/Female?, Q10 - Current Age, Q11 - Which Country do you live in?, Q12 - Highest Level of Education, Q13 – Ethnicity.

# Data cleaning
I conducted data cleaning using the power query function in PowerBI. After assessing the dataset, some issues I observed included;
-irrelevant columns
-empty values
-normalization of columns

# Irrelevant columns & empty values
Columns such as Browser, City, OS,	Country & Referrer contained empty values and termed irrelevant and dropped.
![drop columns](https://user-images.githubusercontent.com/116006674/236623801-88bfaea9-ca22-494b-ad09-9ebee4f12dcb.png)


2.	Normalization of columns
Using the split delimeter option in power query, I splitted the columns which included questions about favourite programming language, country and industry with delimeter set at colon(:), dash(-) and parentheses ‘(‘ respectively to make them readable at a glance and ready for analysis. 

Before                                                                                                               |         After
---------------------------------------------------------------------------------------------------------------------|-------------------------
![q1 before](https://user-images.githubusercontent.com/116006674/236623953-6ef049ce-ae44-430b-9a7a-4a9a090a40da.png) | ![q1 after](https://user-images.githubusercontent.com/116006674/236623954-c378be9f-68ac-47f2-9fde-595e06cad880.png)

Before                                                                                                               |         After
---------------------------------------------------------------------------------------------------------------------|-------------------------
![q5 before](https://user-images.githubusercontent.com/116006674/236624532-a4d55c82-4c99-412e-81c1-a3122eb2f67f.png) |![q5 after](https://user-images.githubusercontent.com/116006674/236624533-bbbf2130-f65f-4558-bb7a-041aa683bd3b.png)


For the current salary column which contained both letters and digits, I first duplicated the column then split it using the ‘digit to non-digit’ option, which split the column into 3 separate columns. Thereafter, I removed the column having just the letter ‘k’ and used ‘replace values’ to remove ‘k’ from the second split column leaving just the digits. Next, I changed the data type of both columns to whole number and using custom column under ‘add column’ tab, I applied DAX function to obtain the average salary from the two columns with digits.

Before                                                                                                               |         After
---------------------------------------------------------------------------------------------------------------------|-------------------------

INSIGHTS
After analysis, I visualized my findings using PowerBI. It was clear that from a total of 630 responders, the Data scientist job title earned the highest average salary while database developers earned the least average salary. The favourite programming language of data professionals is python.
In regards to happiness with salary, data professionals had an average rating of below 5. On average, data professionals voted a 5.74 rating for work/life balance
When asked about the difficulty to break into tech, 43% of the responders voted neutral while 21% of them voted ‘easy’

Conclusion
As a highly competitive field, companies need to look into improving the salary benefits when hiring data professionals. Also the work/life of data professionals can be better through incentives like team bonding activities at work.


