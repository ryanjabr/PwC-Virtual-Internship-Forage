# Task 1 - Call Center Customer Satisfaction | PwC Virtual Case Experience

## Problem Statement

Create a dashboard in Power BI for Claire that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset. 

## Data Sourcing

The dataset used for this analysis was provided by Pwc Switzerland

### Measures

Calculated measures 

Answered : 

```dax
CALCULATE(COUNT(Sheet1[Call Id]),FILTER(Sheet1, Sheet1[Answered (Y/N)]="Y"))
```

Resolved (Y) :

```dax
CALCULATE(COUNT(Sheet1[Call Id]),FILTER(Sheet1,Sheet1[Resolved]="Y"))
```

- Created a new coloumn 'Day Name' which contains the name of the days of the week according to the corresponding entries in the 'Date' coloumn

## Analysis and Insights

- Highest number of calls were answered during the month of January.

- Agent Jim answered and resolved the most no of calls with 536 and 485 respectively.

- A total of 5000 calls were made from which 4054 were answered and 3646 were resolved.

- The most no. of calls received, answered and resolved were on Monday followed by Saturday and Sunday.

- Agent Martha has the highest average rating of 3.47 followed by Dan with 3.45

- Most issues relating to Streaming were resolved (749)
  
# Task 3 - Diversity & Inclusion | PWC Virtual Case Experience

## Problem Statement

- Problem: Human Resources at our telecom client is highly into diversity and inclusion. They’ve been working hard to improve gender balance at the executive management level, but they’re not seeing any progress.

- Objective:
  
   - Define proper KPIs in hiring, promotion, performance and turnover
     
   - Create a visualization for the HR manager that reflects all relevant Key Performance indicators(KPIs) and metrics in the dataset.
     
   -  Define some root causes of their slow progress in improving gender balance at the executive management level 
       
   -  Allows for minimal interaction.
 
## Data Sourcing

The dataset used for this analysis was provided by Pwc Switzerland

## Data Preparation

The dataset was loaded into Microsoft Power BI Desktop for modeling after transformation in Power Query.

The tabulation below shows the Diversity & Inclusion table with its field's names and their description:

- Employee ID	: Represents the unique number of the employee in the dataset
  
- Gender :	Describes the gender of the employee
  
- Job Level after FY20 promotions	: Describes the job level of the employee after being promoted in FY20
  
- New hire FY20? : Describes if the employee is a new hire in FY20

- FY20 Performance Rating :	Represents the performance rating of the employee in FY20
  
- Promotion in FY21? : Describes if the employee is being promoted in FY21
  
- In base group for Promotion FY21 : Describes if the employee is being selected for promotion in FY21
  
- Target hire balance	: Describes the target hire balance of the employee
  
- FY20 leaver? : Describes if the employee is a leaver in FY20
  
- In base group for turnover FY20	: Describes if the employee is in a group for turnover in FY20
  
- Department @01.07.2020	: Describes the department each employee belongs to as of January 7, 2020
  
- Leaver FY :	Describes if the employee is a leaver in an FY
  
- Job Level after FY21 promotions :	Describes the job level of the employee after being promoted in FY21
  
- Last Department in FY20	: Describes the last department each employee belongs in FY20
  
- FTE group :	Describes if the employee belongs to an FTE group
  
- Time type	: Describes the contract type employee
  
- Department & JL group PRA status : Describes the department and JL group PRA status of the employee
  
- Department & JL group for PRA	: Describes the department and JL group PRA of the employee
  
- Job Level group PRA status : Describes the job level group PRA status of the employee
  
- Job Level group for PRA	: Describes the job level group PRA of the employee
  
- Time in Job Level @01.07.2020	: Describes the time in job level of the employee
  
- Job Level before FY20 promotions : Describes the job level of the employee before being promoted in FY20
  
- Promotion in FY20? : Describes if the employee is being promoted in FY20
  
- FY19 Performance Rating	: Describes the performance rating of the employee in FY19
  
- Age group	: Describes the age group of the employee

- Age @01.07.2020	: Represents the age of the employee as of January 07, 2020
  
- Nationality 1	: Describes the nationality of the employee at the state level
  
- Region group : nationality 1	Describes the nationality of the employee at the country level
  
- Broad region group : nationality 1	Describes the nationality of the employee at the regional level
  
- Last hire date : Describes the last hire date of the employee
  
- Years since the last hire	: Represents the number of years since the last hire of the employee
  
- Rand : generates a random number for each entry in the dataset

### Measures

Calculated measures 

Number of Males : 

``` dax
males = CALCULATE(COUNT('Pharma'[Gender]),FILTER('Pharma','Pharma'[Gender]="Male"))
```

Number of Females :

```dax
females = CALCULATE(COUNT('Pharma'[Gender]),FILTER('Pharma','Pharma'[Gender]="Female"))
```

Percentage of Males :

```dax
% males = DIVIDE(Pharma[males],Pharma[males]+Pharma[females])
```

Percentage of Females : 

```dax
% female = DIVIDE(Pharma[females],Pharma[males]+Pharma[females])
```

## Analysis and Insights

The purpose of this dashboard is to serve as self-exploratory for managers, but I still noted some points that I think might be the root causes of their slow progress in improving gender balance at the executive management level :

- A potential factor contributing to the slow progress in achieving gender balance at the executive management level is that the performance evaluations for promotion at management levels may not be entirely objective and honest. This could result in qualified female candidates being overlooked for executive positions, despite their superior performance compared to their male counterparts.

- Employees who were promoted had very low-performance ratings, while those who left had higher ratings.

Dashboard Created (pdf) : [https://github.com/ryanjabr/PwC-Virtual-Internship-Tasks/blob/main/PwC%20HR%20Analysis%20Project.pdf]

