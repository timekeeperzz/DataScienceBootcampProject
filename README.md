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

In the Payment Tier chart, we can see that more people want to stay in the company when the salary range is between 2.30-3.00.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/PaymentTier.png" width="auto">

When employees are compared with their peers according to the age chart, we see that people between the ages of 24-27 prefer to change jobs more (>50%), while more people in the remaining age group prefer to continue their jobs.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/Age.png" width="auto">

For each year of experience, the rate of leaving employees with 0-3 years of experience is between 35-38%. The leaving rates of employees with 4-5 years of experience are 31%, and these rates are 20% and 25% for employees with 6 and 7 years of experience, respectively. We can say that the loyalty rate of employees partially increases as the period spent in the company increases.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/ExperienceInCurrentDomain.png" width="auto"> <img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/ExperienceInCurrentDomain_CrossTab.png" width="auto">


### Bivariate Graphics
I wanted to interpret the data by looking at the heat map graph to better understand the relationship between the columns.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/HeatMap.png" width="auto">

As we can see in the chart, the most relevant columns are Gender and Salary Grade columns. From here we can understand that gender has an impact on salary level. But we can also see that gender and salary grade values do not have much of an impact on the situation of leaving the company.
The values/attributes most relevant to leaving the company are Joining Year to the Company with a correlation score of 0.20 and City with a correlation score of 0.18. We can also say that these two features have an impact on the Education Level (with 0.14 and 0.15 points).

Considering the comments we received from the heat map, I also wanted to examine the Gender – Payment Tier graph.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/Gender_PaymentTier.png" width="auto">

Although the difference is not very clear, we see that men are paid more than women.

Again, in the heat map chart, I came to the idea that the City and Starting Year columns had an impact on the Education Level. Looking at the chart below, most of the employees with a bachelor's degree are from Bangalore. We can say that the number of employees with bachelor's and master's degrees is almost the same among employees living in the capital, New Delhi.
Most of the employees started working in 2017, and most of these employees had a bachelor's degree, while the majority of employees with a master's degree started working in 2017. It can be said that the number of doctoral degrees is almost the same for each year.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/Education_City_JoiningYear.png" width="auto">


## Modeling with Machine Learning
While modeling the data with machine learning, I used the Decision Tree Method and the KNN Method.

### Desicion Tree Model
I used 85% of the data to train the model and 15% to test it. The accuracy rate and error rate of the Decision Tree Model are shown below.

The DecisionTreeClassifier ( ) accuracy score:  80.80
Mean Absolute Error:   0.19197707736389685
The confusion_matrix:  [[403  67]
                        [ 67 161]]
                         
I wanted to add the "Confusion Matrix" method, which I saw in some notebooks I reviewed on Kaggle, to my project. In the chart below, “True Label” represents the 15% we used for testing, while “Predicted Label” represents the predictions of the model.
The Decision Tree Model correctly predicted 403 of the employees who would not quit, but made the wrong decision for 67 employees.
We can see that he came to the right conclusion for 161 of the laid-off employees, but was wrong about 67 employees.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/DFC_Confusion.png" width="auto">

### K-Nearest Neighboor Model
Again, I used 85% of the data to train the model and 15% to test it. The accuracy rate and error rate of the Nearest Neighbor Model are shown below.

The KNeighborsClassifier ( ) accuracy score:  79.66
Mean Absolute Error:   0.2034383954154728
The confusion_matrix:  [[417  53]
                        [ 89 139]]

In the KNN Model, as in the Decision Tree Model, in the chart below, "True Label" represents the 15% we use for testing, while "Predicted Label" represents the predictions of the model.
The KNN Model correctly predicted 417 of the employees who did not quit, but made the wrong decision for 53 employees.
We can see that he came to the right conclusion for 139 of the employees who were laid off, but was wrong about 89 employees.

<img src="https://github.com/timekeeperzz/DataScienceBootcampProject/blob/main/ProjectGraphics/KNN_Confusion.png" width="auto">








