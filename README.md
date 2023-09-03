# Apply filters to SQL queries

<h2>Project description</h2>

As part of my participation in a Google Cybersecurity course, I took on the vital task of enhancing our organization's system security. My role involved ensuring the system's integrity, investigating potential security vulnerabilities, and implementing necessary updates on employee computers. The following steps showcase my utilization of SQL with filters to perform security-related actions.
<br />

<h2>Coding Language</h2>

- <b>SQL</b>

<h2>Retrieve after hours failed login attempts</h2>

There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated.

The following code demonstrates how I created a SQL query to filter for failed login attempts that occurred after business hours:

<img src="https://i.imgur.com/abWAG54.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The first part of the screenshot is my query, and the second part is a portion of the output. This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an AND operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful. The first condition is login_time > '18:00', which filters for the login attempts that occurred after 18:00. The second condition is success = FALSE, which filters for the failed login attempts. 
<br />

<h2>Retrieve login attempts on specific dates</h2>

A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates:

<img src="https://i.imgur.com/Dh1XQ0s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an OR operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is login_date = '2022-05-09', which filters for logins on 2022-05-09. The second condition is login_date = '2022-05-08', which filters for logins on 2022-05-08.
<br />

<h2>Retrieve login attempts outside of Mexico</h2>

I've had the opportunity to analyze our organization's login attempt data. Based on my findings, it appears that there might be a security issue related to login attempts originating from locations outside of Mexico. It is advisable to initiate a detailed investigation into these specific login attempts.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico. 

<img src="https://i.imgur.com/mwrFBqF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred in countries other than Mexico. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with NOT to filter for countries other than Mexico. I used LIKE with MEX% as the pattern to match because the dataset represents Mexico as MEX and MEXICO. The percentage sign (%) represents any number of unspecified characters when used with LIKE. 
<br />

<h2>Retrieve employees in Marketing</h2>

I am presented with the task of collecting information about the computers to be updated for selected employees within the Marketing department. This exercise allows me to apply cybersecurity principles and practices in a real-world context as part of my course learning.

The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building:

<img src="https://i.imgur.com/2nPrVVQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Marketing department in the East building. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with AND to filter for employees who work in the Marketing department and in the East building. I used LIKE with East% as the pattern to match because the data in the office column represents the East building with the specific office number. The first condition is the department = 'Marketing' portion, which filters for employees in the Marketing department. The second condition is the office LIKE 'East%' portion, which filters for employees in the East building.
<br />

<h2>Retrieve employees in Finance or Sales</h2>

The machines for employees in the Finance and Sales departments also need to be updated. Since a different security update is needed, I have to get information on employees only from these two departments.

The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Finance or Sales departments:

<img src="https://i.imgur.com/4S6Uk4H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Finance and Sales departments. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with OR to filter for employees who are in the Finance and Sales departments. I used the OR operator instead of AND because I want all employees who are in either department. The first condition is department = 'Finance', which filters for employees from the Finance department. The second condition is department = 'Sales', which filters for employees from the Sales department.
<br />

<h2>Retrieve all employees not in it</h2>

I'm tasked with the responsibility of acquiring information about employees outside the Information Technology department in order to implement an essential security update. This practical scenario enhances my understanding of cybersecurity concepts within the course curriculum.

The following demonstrates how I created a SQL query to filter for employee machines from employees not in the  Information Technology department:

<img src="https://i.imgur.com/L1xQ5ui.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The first part of the screenshot is my query, and the second part is a portion of the output. The query returns all employees not in the Information Technology department. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with NOT to filter for employees not in this department.
<br />

<h2>Summary</h2>
I effectively employed SQL filters within my queries to extract precise data concerning login attempts and employee machines. Utilizing two separate tables, 'log_in_attempts' and 'employees,' I skillfully harnessed the power of operators such as AND, OR, and NOT to target and retrieve the exact information required for each distinct task. Additionally, I leveraged the LIKE operator in combination with the '%' wildcard to efficiently filter for specific patterns in the data.
<br />


