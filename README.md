# Pewlett-Hackard-Analysis

# Project Overview

### Purpose

The purpose of this analysis is to prepare Pewlett-Hackard, a company with several thousand employees, for the upcoming “silver tsunami”. A large number of employees will begin retiring at a rapid rate in the next few years and the company wants to be prepared with the retirement packages, open positions and employees’ training. In order to ensure a smooth transition this analysis focuses on the following:

1. Identify the retiring employees by their title.
2. Determine the sum of retiring employees grouped by title.
3. Identify the employees eligible for participation in the mentorship program.
4. Determine the number of roles-to-fill grouped by title and department.
5. Determine the number of qualified, retirement-ready employees to mentor the next generation grouped by title and department.

## Resources
Data Source:

 csv files

Software:

PostreSQL,
pgAdmin 4,
Quick DBD


# Results

1. The list of retiring employees

- The table includes employee number, first name, last name, title, from-date and to-date.
- The query returns 133,776 rows.
- The table displays a list of employees who is going to retire in the next few years.
- The list is long and extensive, yet at-a-glance analysis gives us some insights about the query. Some employees appear more than once due to change of title during   their career at Pewlett-Hackard.

![EmployeesTitle](https://user-images.githubusercontent.com/96400887/172651896-595a3f12-00fc-49a4-a9ec-763f0b8004e9.png)

2. The list of retiring employees without duplicates

- The table includes employee number, first name, last name, title, from-date and to-date.
- The query returns 90,398 rows.
- The table displays a list of employees who are going to retire in the next few years.
- In the table each employee is listed only once, by her or his most recent title.

![unique titles](https://user-images.githubusercontent.com/96400887/172652364-6229c939-9685-44ee-94b8-7d18c920043d.png)

3. The number of retiring employees grouped by title

- The table includes employees’ titles and their sum.
- The query returns a cohesive table with 7 rows.
- From this table we can quickly see how many employees with certain title will retire in the next few years.

![retiering titles](https://user-images.githubusercontent.com/96400887/172652643-d7970f17-ff97-41ea-a015-158e99df4075.png)








