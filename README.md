# Pewlett-Hackard-Analysis

# Project Overview

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

4. The employees eligible for the mentorship program

- The table contains employee number, first name, last name, birth date, from date, to date and title.
- The query returns 1,549 rows.
- The table displays a list of employees who is eligible for the mentorship program.

![Menthorship](https://user-images.githubusercontent.com/96400887/172721968-4bbcd886-aac1-407a-aa91-0fcefdc45013.png)


# Summary

- As the company is preparing for the upcoming "silver tsunami" a good planning is essential, especially when such a large number of the employees is involved. Reports above give a good insight about the number of the employees that are about to retire and hold specific title. However, I believe that additional break down per department will be beneficial for the company. In this case headquarters can see what to expect in each department separately. In order to retrieve department name information, I merged additional table departments into existing table retirement_titles with the inner join. After removing the duplicates, with DISTINCT ON command, the table was ready to be used for additional queries.
-  Table with retirement-ready employee’s data with added department name

![Extra_TitlesAndDepartment](https://user-images.githubusercontent.com/96400887/172720655-37022a79-d085-4c6e-a42b-78a87f85ac86.png)

- How many roles will need to be filled as the "silver tsunami" begins to make an impact?
The table retirement titles contains all the information about the employees that are about to retire in the next four years. To get the number of positions that will be open in next four years I ran additional query that breaks down how many staff will retire per department. Since every department will be affected in some way this query gives more precise numbers what each department can expect and how many roles will need to be filled.
- Sum of retirement-ready employees group by title and department.

![Extra_RolesToFill](https://user-images.githubusercontent.com/96400887/172721012-02569295-1cae-4312-b0c2-0bb8ce213f79.png)












