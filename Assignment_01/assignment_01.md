## [Quiz: 01]()
Create Database 	: 	Records
Create Table		: 	Emp
![Question](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Assignment_01/ScreenShots/q.PNG)

Perform the following queries:

1.	Show all records in descending order with respect to Ename.
```
SELECT * FROM emp ORDER BY emp_name DESC;
```
2.	Find records in which EName begins with ‘S’ and ends to ‘n’.
```
SELECT * FROM emp WHERE emp_name LIKE 'S%n';
```
3.	Find records in which EName contains ‘ba’ in middle.
```
SELECT * FROM emp WHERE emp_name LIKE '%ba%';
```
4.	Create a query to display unique jobs from the Emp table.
```
SELECT DISTINCT job FROM emp;
```
5.	How many employees are in Department Number 10?
```
SELECT * FROM emp WHERE dept_no = 10;
```
6.	List all employees who are either manager or salesman.
```
SELECT * FROM emp WHERE job IN ('manager', 'salesman');
```
7.	How many records do we have?
```
SELECT COUNT(*) AS total_records FROM emp;
```
8.	How many jobs do we have?
```
SELECT COUNT(DISTINCT job) FROM emp;
```
9.	How many managers, clerks and salesmen are working in the company?
```
SELECT * FROM emp WHERE job IN ('manager', 'clerk', 'salesman');
```
10.	Show all records whose salary is more than 2000 and less than 6000.
```
SELECT * FROM emp WHERE salary BETWEEN 2000 AND 6000;
```
11.	Write a query to display maximum, minimum, sum and average of salaries.
```
SELECT MAX(salary) AS max_salary, MIN(salary) AS min_salary, 
SUM(salary) AS total_salary, AVG(salary) AS avg_salary FROM emp;
```
12.	List all records with EName, Salary, Commission and Total Salary after commission.
```
SELECT emp_name, salary, commision, (salary + commision) AS total_salary FROM emp;
```
13.	List all ‘Salesman’ and add 500 to their salaries, also change the column heading to SalaryWithBonus.
```
SELECT emp_name, job, (salary + 500) AS salary_with_bonus FROM emp 
WHERE job = 'Salesman';
```
14.	Create a query to display EName, Salary, ZakatDeductionAmount i.e. 2.5%, SalaryAfterZakat from Emp.
```
SELECT emp_name, salary, (salary * 0.025) AS salary_after_zakat FROM emp;
```
15.	Write a query to delete all records from Emp.
```
DELETE FROM emp;
```
16.	Write a query to delete table Emp.
```
DROP TABLE Emp;
```
17.	Write a query to delete the database.
```
DROP DATABASE quiz
```