Case Study 2 Codebook
=====================

Introduction
------------

This codebook contains information about the raw datasets, how it was
cleaned, and the tidy datasets.

Raw Dataset:
------------

-   CaseStudy2-data.xlsx

Variables for Raw Dataset:
--------------------------

-   Age- Indicates the age the employee is
-   Attrition- Indicates if voluntary employee turnover was present
    ('yes' or 'no')
-   BusinessTravel- Indicated the frequency the employee traveled
    ('Travel\_Rarely', 'Travel\_Frequently', 'Non-Travel')
-   DailyRate- Rate the employee makes per day
-   Department- The department that the employee works in
-   DistanceFromHome- Distance that the employee lives from work in
    miles
-   Education- Highest educational degree obtained by the employee
    (1=Below College, 2=College, 3=Bachelor, 4=Master, and 5=Doctor)
-   EducationField- Indicates the educational field the employee studied
-   EmployeeCount- Number of employees the observation is referring to
-   EmployeeNumber- Employee's assigned Company number
-   EnvironmentSatisfaction- An indicator of employee's satisfaction
    level with their work environment ('1'=low, '2'=medium, '3'=high,
    '4'=very high)
-   Gender- Indicates the employees gender
-   HourlyRate- Rate the employee makes per hour
-   JobInvolvement- An indicator of employee's involvement level within
    the Company ('1'=low, '2'=medium, '3'=high, '4'=very high)
-   JobLevel- Level of employee's job from ('1','2','3','4',or '5')
-   JobRole- Indicates the employee's role at the Company
-   JobSatisfaction- An indicator of employee's satisfaction level with
    their job ('1'=low, '2'=medium, '3'=high, '4'=very high)
-   MaritalStatus- Indicates employee's marital status ('Single',
    'Married', or 'divorced')
-   MonthlyIncome- Employee's income per month from the Company
-   MonthlyRate- Employee's rate per month
-   NumCompaniesWorked- Number of different companies the employee has
    worked for
-   Over18- Indicates if the employee is over 18 ('yes' or 'no')
-   OverTime- Indicates whether the employee works overtime ('yes' or
    'no')
-   PercentSalaryHike- Percent of employee's salary hike
-   PerformanceRating- An indicator of employee's performance with
    ('1'=unsatisfactory, '2'=satisfactory, '3'=excellent,
    '4'='outstanding)
-   RelationshipSatisfaction- An indicator of how satisfied the employee
    is with their relationships with coworkers ('1'=low, '2'=medium,
    '3'=high, '4'=very high)
-   StandardHours- Number of regular hours worked during the period
-   StockOptionLevel- Level of stock options offered to the employee by
    the Company
-   TotalWorkingYears- Total number of years the employee has worked in
    their career
-   TrainingTimesLastYear- Number of training hours the employee
    attended last year
-   WorkLifeBalance- Indicates the employee's work-life balance rating
    ('1'=low, '2'=medium, '3'=high '4'=very high)
-   YearsAtCompany- Number of years the employee has worked for the
    company
-   YearsInCurrentRole- Number of years the employee has been in their
    current role at the company
-   YearsSinceLastPromotion- Number of years since the employee's last
    promotion
-   YearsWithCurrManager- Number of years the employee has worked for
    their current manager

Packages Used for Cleaning Dataset:
-----------------------------------

-   library(dplyr)
-   library(readxl)

Steps for tidying data (Code is contained in "data\_processing.R"):
-------------------------------------------------------------------

1.  Read in CaseStudy2-data.xlsx
2.  Process data definitions
3.  Remove factors that only have one level
4.  Remove protected class variables
5.  Remove meaningless variables

analysis\_df
------------

This dataset was obtained from the raw dataset. Variables that are
protected by law were removed (Age, Gender and Marital Status) Variables
that are meaningless were removed (Employee Number, Over 18, Standard
Hours)

CurrentEmployees
----------------

This dataset was obtained from analysis\_df This data removed all rows
where attrition was 'yes'
