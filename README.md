# Sales-of-Retail-Store

## Tables of Contents
- [Project Overview](https://github.com/Phatolic/HR#project-overview)
- [Data Sources](https://github.com/Phatolic/HR#data-sources)
- [Data Cleaning/Preparation](https://github.com/Phatolic/HR#data-cleaningpreparation)
- [Data Analysis](https://github.com/Phatolic/HR#data-analysis)
- [Dashboard](https://github.com/Phatolic/HR#dashboarding)
- [Limitations](https://github.com/Phatolic/HR#results#limitations)

### Project Overview

This data analysis project aims to provide insights into the performance of the retail store. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's sales.  

---
### Data Sources

<b>Location Table</b>  

- 

---
### Data Cleaning/Preparation

#### Power Query
<b>- Transformed data loads to Transformed data tab in the workbook.  </b>  

<b>Columns:</b>  

- Age_Group: Derived from column Age and divided into 5 different groups.  

- Performance Status: Derived from column Performance Rating and divided into High and Low categories.  

- Job Satisfaction Status: Derived from column Job Satisfaction with 1 as Very Satisfied, 2 as Satisfied, 3 as Dissatisfied and 4 as Very Dissatisfied.  

- Distance Status: Derived from column Distance From Home with less than or equals to 10 is Near-by, more than 10 and less than or equals to 20 is Far, and more than 20 is Very-far.
  
---
### Data Analysis   
<b>- Pivot tables created in Analysis tab in the workbook.  </b>  

> Analysis the employees has left the company. (Attrition column value is Yes)

1. Total Employees

    ![TotalEmp](https://github.com/Phatolic/HR/assets/144981161/942c5d29-20e2-4556-9773-9117be57a3d1)

2. Employee Attrition Rate 

    ![EmpAttritionRate](https://github.com/Phatolic/HR/assets/144981161/c54242e5-fead-41d9-8b92-127991204f52)

3. Average Age

    ![AvgAge](https://github.com/Phatolic/HR/assets/144981161/038e0868-7c0a-4f2d-8593-2938a0554c22)

4. Business Travel

    ![BusinessTravel](https://github.com/Phatolic/HR/assets/144981161/22c40f43-caac-47ce-b03d-ef1d7366bf0a)

5. Employee Performance Status

   ![PerformanceStatus](https://github.com/Phatolic/HR/assets/144981161/cbb2aa83-ccb7-4ca8-9027-e90ddb1606d7)

6. Employee Work Distance

    ![WorkDis](https://github.com/Phatolic/HR/assets/144981161/3fd0a6eb-bae3-4187-82ac-30d36791c3f0)

7. Employee Job Role
   
    ![JobRole](https://github.com/Phatolic/HR/assets/144981161/e77f0302-8d9b-4cf9-bc27-0630a2279095)

9. Employee Education
    
    ![Education](https://github.com/Phatolic/HR/assets/144981161/6433a0c8-82b0-45b4-ab5f-334cd85b8a45)

11. Age Group & Gender

    ![AgeGr_Gender](https://github.com/Phatolic/HR/assets/144981161/bf4d7c3d-d33f-4cc0-b8d5-a7ab3dc81d14)

---
### Dashboarding

<b>- Charts created in Charts tab in the workbook.  </b>
- Format the charts and build the dashboard.  
- Add slicers.
  
    ![Dashboard](https://github.com/Phatolic/HR/assets/144981161/54b19efc-6613-4537-850a-3db62ffe4a18)
   
### Results

<b>-> </b>The high-performed employees are more likely to leave the company than the low_performed ones with 413 employees compared to only 79, respectively. That is accounted for nearly 84% of the left employees.  

<b>-> </b>The closer the distance from the company to the employees' homes, the higher the number of employees who left the company. Need to dig deeper into this situation.

<b>-> </b>Males from every age groups tend to leave the company more frequently than the females.

##### It seems the issue is more company-generated. Should check again the policies for employees and related resources.
### Limitations

- Suggest to look into the environment satisfaction of the employees.

- Look into the monthly income of employees to see if the employee is paid correctly.

