# ANALYSIS OF WHY EMPLOYEES LEAVE THEIR JOBS - Data Analysis and Modeling

## 1- About Project

For the project assignment, I chose a data set that I thought was suitable for entry level and modelable. There are a total of 4653 rows and 9 columns in this data set, whose target variable is whether employees in a company quit their jobs or not. The names of these columns and what they mean are as follows.

**Education:** Education Level(Bachelors, Masters and PHD)

**Joining year:** Year of starting work

**City:** Hometowns of Employees

**PaymentTier:** Salary Tier

**Age:** Age of Employees

**Gender:** Gender (Male, Female)

**EverBenched:** Indicates whether an employee is given a temporary job (except for his/her responsibility) (yes or no)

**Eperience in current domain:** Years of experience in the company (in years)

**LeaveOrNot:** Whether they left the job (1: To leave 0: Not to leave)

## 2-	Exploratory Data Analysis (EDA)

First, I checked whether there was a null value in any column in the data set, and then I checked whether there was an outlier value.
There were lines that repeated themselves. These lines made almost no deviation in the data analysis, that is, they did not lead to a change of opinion, but they reduced the accuracy value in the modeling part by at least 10%. That's why I decided not to delete repetitive lines.

### Univariate Graphics
I first examined the data based on categorical columns. I interpreted each of them through graphics.
The graph showing the number of our target variable is as follows.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/LeaveOrNotCounts.png" width="auto">

As we can see in the chart below; Almost half of those with a master's degree have left their jobs, while the majority of employees with a bachelor's degree and doctorate continue to work in the company.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/Education.png" width="auto">

If we make a comparison considering the city variable; While half of the employees from Pune City have left their jobs, most of the employees from Bangalore and New Delhi have remained with the company.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/City.png" width="auto">

While approximately half of female employees continue to work, the majority of male employees have decided to stay at the company.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/Gender.png" width="auto">

The number of employees taking on extra duties is small, but we can say that the EverBenched feature has an impact on employee turnover. Almost half of the employees who took on extra duties left their jobs.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/EverBenched.png" width="auto">

After interpreting the categorical columns, I also interpreted the numerical columns through graphics.
I made a comparison based on Joining Year feature. When we look at the graph in question, we see that the people who left their jobs were in 2015, 2017 and 2018. But at the same time, if we make a comparison among the people who started working in 2017, most people did not leave their jobs, and almost all of the employees who started in 2018 left their jobs. We can say that the years with the lowest layoff rate were 2012 and 2016.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/JoiningYear.png" width="auto">


