# Analyzing the Connection Between Attrition and Employees in Corporations: Power BI
Model generation to identify the most important variables to use in predicting employees' voluntary exit from a company. 

## Problem Statement:
The purpose of this project is to analyse the relationship between attrition and employees in an organisation using Power BI. 

Attrition is an unavoidable occurrence in the work environment. There will come a time when an employee wants to leave an organization – either for personal or professional reasons. (BasuMallick, 2021) describes attrition as the act of employees discontinuing working in their place of engagement through instances such as resignation and are not immediately replaced.

The HR department is one of the key units of an organization that’s involved with taking care of employees – including, but not limited to, recruitment, compensation, work policies, employee benefits.

A practical use of this project is to help organisations develop effective employee retention strategies through the identification of underlying factors that contribute to attrition. 

It also finds use in the refinement of recruitment processes. By identifying factors that lead to attrition, organisations could focus on attracting candidates who align with the organization's values and have a higher likelihood of long-term commitment.

The primary tool used for this project is Python 3, along with an extensive array of libraries and packages available for the manipulation of data, and development of predictive modeling algorithms. 

The tool of visualization used is Power BI. This is a powerful data integration and interactive visualization software that aids in the effective analysis of this project. 

## Dataset Description:
The dataset utilized in this project comprises 35 columns and 1470 rows. This dataset is suitable for my research as it encompasses an adequate number of independent and dependent variables that can be analyzed to effectively address the research questions. 

### Variables Description

| S/N |	Variable | Type | Description |
|:---|:---|---|---|
| **1**|	Work Life Balance	| Categorical	| This depicts how much time an employee can allocate between personal life and working in the office (1 - "Bad", 2 - "Good", 3 - "Better", 4 - "Best"). 
| **2**| Gender	| Categorical	| The sexes of employees – Men and women. 
|**3**|	Monthly Income	|Numerical|	The amount of money earned by workers. 
|**4**|	Attrition|	Categorical|	Information on workers leaving their jobs.
|**5**|	Job Satisfaction Level|	Categorical|	The extent people in the organisation are happy with their work duties (1 - "Low", 2 - "Medium", 3 - "High", 4 - "Very High").
|**6**|	Job Role|	Categorical|	Specific tasks that are performed by workers in the company. 
|**7**|	Education|	Categorical|	How advanced an individual has gone in terms of academics. 
|**8**|	Years at Company|	Numerical| The amount of working time that has been spent in the corporation by an employee. 
|**9**|	Age | Numerical|	The age of a worker. 
|**10**| Department|	Categorical|	The business unit where people work in the organization. 
|**11**| Marital Status|	Categorical|	An indication of an employee having a partner or not. 
|**12**| Hourly Rate|	Numerical|	Rate of pay per hour for someone on the job.
|**13**|	Standard Hours|	Categorical|	Established work time for a period (always 80 in this dataset).
|**14**|  Business Travel| Categorical | Frequency of business travel.
|**15**| Daily Rate| Numerical| Employee's daily rate of pay.
|**16**| Distance From Home| Numerical| Distance from employee's home to workplace.
|**17**| Education Field| Categorical| Field of education of an employee.
|**18**| Employee Count| Numerical| Number of employees with the same value (always 1 in this dataset).
|**19**| Employee Number| Numerical| Unique identifier for each employee.
|**20**| Environment Satisfaction| Categorical| Employee's satisfaction with the work environment (1 - "Low", 2 - "Medium", 3 - "High", 4 - "Very High").
|**21**| Job Involvement| Categorical| Employee's level of job involvement (1 - "Low", 2 - "Medium", 3 - "High", 4 - "Very High").
|**22**| Job Level| Numerical| Employee's job level.
|**23**| Monthly Rate| Numerical| Employee's monthly rate of pay.
|**24**| Num of Companies Worked| Numerical| Number of companies an employee has worked for prior to the current job.
|**25**| Over 18| Categorical| Whether an employee is over 18 years old or not.
|**26**| Over Time| Categorical| Whether an employee works overtime or not.
|**27**| Percent Salary Hike| Numerical| Percentage increase in an employee's salary.
|**28**| Performance Rating| Categorical| Employee's performance rating (1 - "Low", 2 - "Good", 3 - "Excellent", 4 - "Outstanding").
|**29**| Relationship Satisfaction| Categorical| Employee's satisfaction with work relationships (1 - "Low", 2 - "Medium", 3 - "High", 4 - "Very High").
|**30**| Stock Option Level| Numerical| Employee's stock option level.
|**31**| Total Working Years| Numerical| Total number of years an employee has worked.
|**32**| Training Times Last Year| Numerical| Number of times an employee received training last year.
|**33**| Years in Current Role| Numerical| Number of years an employee has been in the current role.
|**34**| Years Since Last Promotion| Numerical| Number of years since an employee's last promotion.
|**35**| Years With Current Manager| Numerical| Number of years an employee has worked with the current manager.

The independent variables (numerical) chosen for the prediction are: `['Age', 'MonthlyIncome', 'HourlyRate', 'MonthlyRate', 'PercentSalaryHike', 'TotalWorkingYears', 'TrainingTimesLastYear', 'YearsAtCompany', 'YearsInCurrentRole', 'YearsSinceLastPromotion', 'YearsWithCurrManager']`

The target (dependent) variable was `['Attrition']`. Due to the inability of the model to use a categorical variable for its algorithm generation, I transformed the attrition variable to numerical - labelled `['Attrition_Coded']`. This was achieved by creating a new column using Pandas with the "np.where" function.

## Exploratory Data Analysis: 
This involves looking at the data summaries and visualizations to:
1.	Analyse the data
2.	Discover patterns and relationships between the features
3.	Identify the data types
4.	Clean up the data

### Practical Steps Taken: 
The technology used for the Exploratory Analysis is the Python Programming Language, in a Jupyter Notebook Environment. Within the Python ecosystem, various libraries and packages were used, and are listed below:

1.	Pandas
2.	Numpy
3.	Matplotlib

Reports and visualizations I generated on the Power BI platform provided invaluable business insights to communicate to stakeholders. 

Initially, the data was read into the Python Environment using the pandas package, which provided me the functionality of viewing a description of the dataset. 

Below is a screenshot of the code used for loading the data into Python.

![Loading_Data](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/78c618fd-a62f-4334-aa58-93cf12f4d1dd)








