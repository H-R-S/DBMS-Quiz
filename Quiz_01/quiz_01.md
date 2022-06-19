## [Quiz: 01](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/quiz_01.md)
Create Database 	: 	Records

Create Table		: 	Emp


![Question](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q.PNG)

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
### Complete Query:
```
CREATE DATABASE Quiz

CREATE TABLE emp(
	emp_no INT (12) NOT NULL PRIMARY KEY,
	emp_name VARCHAR (56) NOT NULL,
	job CHAR (23) NOT NULL, 
	manager_no INT (20),
	hire_date VARCHAR (10) NOT NULL,
	salary INT (20) NOT NULL,
	commision INT (23),
	dept_no INT (23) NOT NULL
);
 
INSERT INTO emp (emp_no, emp_name, job, manager_no, hire_date, salary, commision, dept_no)
VALUES (1001, 'Gohar', 'Salesman', 512, '18-Dec-11', 1600, 400, 20),
       (1002, 'Ahmed', 'Clerk', 511, '28-Nov-11', 1250, NULL, 10),
       (1003, 'Shahid', 'Manager', 505, '11-Jun-11', 10000, NULL,  20),
       (1004, 'Toqeer', 'Salesman', 512, '15-Dec-10', 2700, 300, 20),
       (1005, 'Asif', 'Manager', 505, '18-Dec-10', 12000, NULL, 15),
       (1006, 'Babar', 'Salesman', 512, '14-Nov-10', 4000, 500, 20),
       (1007, 'Kashif', 'President', NULL, '21-Oct-10', 20000, NULL, 10),
       (1008, 'Zubair', 'Manager', 505, '8-Dec-09', 15000, NULL,  10),
       (1009, 'Yasir', 'Clerk', 511, '18-Dec-09', 1650, NULL, 15),
       (1010, 'Salman', 'Salesman', 512, '10-May-09', 5300, 700, 20),
       (1011, 'Hafeez', 'Clerk', 511, '1-Jan-09', 1500, NULL, 15);

/*1.Show all records in descending order with respect to Ename.*/
SELECT * FROM emp ORDER BY emp_name DESC;

/*2.Find records in which EName begins with ‘S’ and ends to ‘n’.*/
SELECT * FROM emp WHERE emp_name LIKE 'S%n';

/*3.Find records in which EName contains ‘ba’ in middle.*/
SELECT * FROM emp WHERE emp_name LIKE '%ba%';

/*4.Create a query to display unique jobs from the Emp table.*/
SELECT DISTINCT job FROM emp;

/*5.How many employees are in Department Number 10?*/
SELECT * FROM emp WHERE dept_no = 10;

/*6.List all employees who are either manager or salesman.*/
SELECT * FROM emp WHERE job IN ('manager', 'salesman');

/*7.How many records do we have?*/
SELECT COUNT(*) AS total_records FROM emp;

/*8.How many jobs do we have?*/
SELECT COUNT(DISTINCT job) FROM emp;

/*9.How many managers, clerks and salesmen are working in the company?*/
SELECT * FROM emp WHERE job IN ('manager', 'clerk', 'salesman');

/*10.Show all records whose salary is more than 2000 and less than 6000.*/
SELECT * FROM emp WHERE salary BETWEEN 2000 AND 6000;

/*11.Write a query to display maximum, minimum, sum and average of salaries.*/
SELECT MAX(salary) AS max_salary, MIN(salary) AS min_salary, 
SUM(salary) AS total_salary, AVG(salary) AS avg_salary FROM emp;

/*12.List all records with EName, Salary, Commission and Total Salary after commission.*/
SELECT emp_name, salary, commision, (salary + commision) AS total_salary FROM emp;

/*13.List all ‘Salesman’ and add 500 to their salaries, also change the column heading to SalaryWithBonus.*/
SELECT emp_name, job, (salary + 500) AS salary_with_bonus FROM emp 
WHERE job = 'Salesman';

/*14.Create a query to display EName, Salary, ZakatDeductionAmount i.e. 2.5%, SalaryAfterZakat from Emp.*/
SELECT emp_name, salary, (salary * 0.025) AS salary_after_zakat FROM emp;

/*15.Write a query to delete all records from Emp.*/
DELETE FROM emp;

/*16.Write a query to delete table Emp.*/
DROP TABLE Emp;

/*17.Write a query to delete the database.*/
DROP DATABASE quiz
```
### ScreenShots:
#### Question: 01
![Q1](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q1.PNG)
#### Question: 02
![Q2](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q2.PNG)
#### Question: 03
![Q3](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q3.PNG)
#### Question: 04
![Q](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q4.PNG)
#### Question: 05
![Q5](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q5.PNG)
#### Question: 06
![Q6](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q6.PNG)
#### Question: 07
![Q7](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q7.PNG)
#### Question: 08
![Q8](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q8.PNG)
#### Question: 09
![Q9](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q9.PNG)
#### Question: 10
![Q10](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q10.PNG)
#### Question: 11
![Q11](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q11.PNG)
#### Question: 12
![Q12](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q12.PNG)
#### Question: 13
![Q13](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q13.PNG)
#### Question: 14
![Q14](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q14.PNG)
#### Question: 15
![Q15](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q15.PNG)
#### Question: 16
![Q16](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q16.PNG)
#### Question: 17
![Q17](https://github.com/H-R-S/DBMS-Quiz-AND-Assignments/blob/main/Quiz_01/ScreenShots/q17.PNG)