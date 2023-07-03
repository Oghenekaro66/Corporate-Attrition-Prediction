# Analyzing the Link Between Attrition and Employees in Corporations

## Problem Statement
The purpose of this project is to analyse the relationship between attrition and employees in an organisation. 

Attrition is an unavoidable occurrence in the work environment. There will come a time when an employee wants to leave an organization – either for personal or professional reasons. (BasuMallick, 2021) describes attrition as the act of employees discontinuing working in their place of engagement through instances such as resignation and are not immediately replaced.

The HR department is one of the key units of an organization that’s involved with taking care of employees – including, but not limited to, recruitment, compensation, work policies, employee benefits.

A practical use of this project is to help organizations develop effective employee retention strategies through the identification of underlying factors that contribute to attrition. 

It also finds use in the refinement of recruitment processes. By identifying factors that lead to attrition, organizations could focus on attracting candidates who align with the organization's values and have a higher likelihood of long-term commitment.

The primary tool used for this project is Python 3, along with an extensive array of libraries and packages available for the manipulation of data, and development of predictive modelling algorithms. 

The tool of visualization used is Power BI. This is a powerful data integration and interactive visualization software that aids in the effective analysis of this project. 

## Dataset Description
The dataset utilized comprises 35 columns and 1470 rows. This dataset is suitable for my research as it encompasses an adequate number of independent and dependent variables that can be analyzed to effectively address the research questions. 

### Variables Description

| S/N |	Variable | Type | Description |
|:---|:---|---|---|
| **1**|	Work Life Balance	| Categorical	| This depicts how much time an employee can allocate between personal life and working in the office (1 - "Bad", 2 - "Good", 3 - "Better", 4 - "Best"). 
| **2**| Gender	| Categorical	| The sexes of employees – Men and women. 
|**3**|	Monthly Income	|Numerical|	The amount of money earned by workers. 
|**4**|	Attrition|	Categorical|	Information on workers leaving their jobs.
|**5**|	Job Satisfaction Level|	Categorical|	The extent people in the organization are happy with their work duties (1 - "Low", 2 - "Medium", 3 - "High", 4 - "Very High").
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

The target (dependent) variable was `['Attrition']`. Due to the inability of the model to use a categorical variable for its algorithm generation, I transformed the attrition variable to numerical - labelled as `['Attrition_Coded']`. This was achieved by creating a new column using Pandas with the "np.where" function.

## Exploratory Data Analysis 
This involves looking at the data summaries and visualizations to:
1.	Analyse the data
2.	Discover patterns and relationships between the features
3.	Identify the data types
4.	Clean up the data

### Practical Steps Taken 
The technology used for the Exploratory Analysis is the Python Programming Language, in a Jupyter Notebook Environment. Within the Python ecosystem, various libraries and packages were used, and are listed below:

1.	Pandas
2.	Numpy
3.	Matplotlib

Reports and visualizations I generated on the Power BI platform provided invaluable business insights to communicate to stakeholders. 

Initially, the data was read into the Python Environment using the pandas package, which provided me the functionality of viewing a description of the dataset. 

Below is a screenshot of the code used for loading the data into Python.

![Loading_Data](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/78c618fd-a62f-4334-aa58-93cf12f4d1dd)

---

### Data Cleaning
Perform a preliminary data inspection and data cleaning.

a. Check for missing data and formulate an apt strategy to treat them.

b. Remove duplicate data records.

![Duplicates and Null Values](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/f5469dfe-25f8-49bb-a59c-9a3fb7769e51)

### Choosing the Best Model 
The next phase was selecting the best model to deploy to identify the columns, in descending order, that are important for attrition prediction. I ran 3 different models to get the best for prediction purposes. The choice of algorithms are:  

1.	Linear Regression
2.	Random Forest Regressor 
3.	Gradient Boosting Regressor
   
The Evaluation metric used for these models is the Mean Squared Error.

![LR_Model](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/8500b02b-4510-403f-b594-5260ef520105)

---

![RF_Model](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/6d34e0ae-0c02-47b8-8a9c-0c3f3b268b57)

---

![GB_Model](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/5251bb47-982a-4dd0-9d66-f4e5319979af)

---

The best model is the Gradient Boosting Regressor model as it generated the lowest mean square error value of: 0.106131788

### Feature Importances
This is displaying the important variables and how each feature performs with the best model selected in making predictions.

![Feature Importances](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/2ff67db0-67fd-4bf4-b387-6a395bbac426)

---

Deploying the Gradient Boosting Regressor model, it can be deduced that `['MonthlyIncome', 'MonthlyRate', 'Age', 'HourlyRate', 'YearsSinceLastPromotion']` are the top 5 predicted features for employee attrition. 

By means of visually conveying this information , I used the Matplot library (matplotlib.pyplot) to create a horizontal bar chart for the graphical representation of the results. 

![Matplotly_Feature Importances](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/a8bbb28c-bc22-4a9b-a8e6-aa2316482a67)

---

Finally, with the aid of seaborn and matplotlib, I plotted a heatmap of the feature importances using the computed correlation matrix. This is to show the strength of association between the variables and also those that are strongly related. 

![Heatmap](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/938ddc6f-edcc-42b1-9a96-4a58c7ecc386)

---

## Visualization and Business Intelligence
This is the generation of visual reports that provide meaningful insights into different features within the dataset.

![BI_I](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/c56e0381-732a-41ea-bc53-2453d5d8f1d5)


---

![BI_II](https://github.com/Oghenekaro66/Corporate-Attrition-Prediction/assets/116779227/e42878b2-36c9-4301-8af3-65743bcef73d)


---

Based on the data analysis, notable findings include:

1. The data indicates a higher attrition rate among male employees compared to female employees. This observation may be influenced by the lower monthly income of male employees compared to their female counterparts.

2. The trend of employees departing from their organizations gradually diminished as their time with the company extended. This pattern can be attributed to the noteworthy correlation between prolonged years of service and higher monthly salary levels within the organization.

3. As the age and average total working years of an employee increased, the leaving of individuals diminished significantly. This remarkable trend can be attributed to a compelling positive relationship between years of service and monthly earnings.

## Recommendations 
Based on the comprehensive analysis conducted on this project and dataset, I have identified a set of actionable strategies and interventions that organizations can adopt to effectively mitigate attrition and enhance employee retention. These insights hold the potential to drive significant positive outcomes for organizational success and employee satisfaction.

They are delineated hereunder:

1. Addressing gender-based wage disparity could potentially help reduce the attrition rate among male employees. By rectifying any existing pay gaps and promoting gender equality in terms of compensation, the organization can create a more inclusive and supportive work environment. This, in turn, can lead to improved employee satisfaction, engagement, and ultimately, lower attrition rates among both male and female employees.

2.  Recognizing the value of employee tenure and its positive impact on employee retention, the organization can focus on implementing initiatives to enhance career growth opportunities, professional development programs, and performance-based rewards. These can foster a motivating work environment for the employees that encourages them to stay for the long term.

3.  Recognizing and rewarding employees for their long-term commitment and dedication is of paramount importance, as it plays a crucial role in fostering higher retention rates. Emphasizing rewards, such as providing competitive salaries and benefits that align with employees' increasing value over time, can be a pivotal step in achieving this goal. By adopting such measures, organizations can significantly enhance employee satisfaction, engagement, and loyalty, which in turn leads to reduced turnover.

## Conclusion
This project delved into the critical issue of employee attrition and retention within organizations. Through extensive data analysis and machine learning techniques, we gained valuable insights into the factors that influence attrition rates.

The findings revealed key drivers of employee attrition, such as income, years of experience, and tenure in a company. Armed with this knowledge, organizations can proactively implement targeted strategies to reduce attrition and bolster employee retention.

By adopting evidence-based interventions, such as improving compensation, recognizing employee achievements, and providing growth opportunities, organizations can create a more conducive and fulfilling work environment. This, in turn, fosters a stronger sense of loyalty and engagement among employees, ultimately leading to improved retention rates and a more productive workforce.

Overall, the project emphasizes the importance of data-driven decision-making in addressing employee attrition challenges. Armed with the right insights and strategies, organizations can build a resilient workforce, enhance employee satisfaction, and secure long-term success.











