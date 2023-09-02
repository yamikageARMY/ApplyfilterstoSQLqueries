# Apply filters to SQL queries

<h2>Project description</h2>
As part of my participation in a Google Cybersecurity course, I took on the vital task of enhancing our organization's system security. My role involved ensuring the system's integrity, investigating potential security vulnerabilities, and implementing necessary updates on employee computers. The following steps showcase my utilization of SQL with filters to perform security-related actions.
<br />

<h2>Coding Language</h2>

- <b>SQL</b>

<h2>Retrieve after hours failed login attempts</h2>

There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated.

The following code demonstrates how I created a SQL query to filter for failed login attempts that occurred after business hours.

<img src="https://i.imgur.com/abWAG54.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The first part of the screenshot is my query, and the second part is a portion of the output. This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an AND operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful. The first condition is login_time > '18:00', which filters for the login attempts that occurred after 18:00. The second condition is success = FALSE, which filters for the failed login attempts. 

<br />

