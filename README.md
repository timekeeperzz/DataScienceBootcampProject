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

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/LeaveOrNotCounts.png)" width="auto">



