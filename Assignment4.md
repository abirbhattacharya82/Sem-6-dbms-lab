We will be Using The Table made in Assignment 1 for this Assignment

Q1) Calculate the average salary of all employees.
```
select AVG(Sal) from Emp;
```

Q2) Calculate the average salary of all managers.
```
select AVG(Sal) from Emp where Job='Manager';
```

Q3) Calculate the total salary of all employees.
```
select Sum(Sal) from Emp;
```

Q4) Calculate the total salary of all managers.
```
select Sum(Sal) from Emp where Job='Manager';
```

Q5) Find the minimum salary earned by the employees.
```
select Min(Sal) from Emp;
```

Q6) Find the maximum salary earned by the employee.
```
select Max(Sal) from Emp;
```

Q7) Find the minimum salary earned by clerk.
```
select Min(Sal) from Emp where Job='Clerk';
```

Q8) Find the maximum salary earned by salesman.
```
select Max(Sal) from Emp where Job='Salesman';
```

Q9) Find the minimum, maximum and average salary earned by an employee.
```
select Max(Sal), Min(Sal), AVG(Sal) from Emp;
```

Q10) Find the minimum, maximum and average salary earned by a clerk.
```
select Max(Sal), Min(Sal), AVG(Sal) from Emp where Job='Clerk';
```

Q11) List the total number of employees and average salaries of the different department.
```
select count(*) from Emp;
select AVG(Sal), Job from Emp group by Job;
```

Q12) Calculate total no. of employees.
```
select count(*) from Emp;
```

Q13) Calculate total no. of managers
```
select count(*) from Emp where Job='Manager';
```

Q14) List the details of all managers in ascending order of joining dates.
```
select * from Emp where Job='Manager' order by Hiredate;
```

Q15) List the average salary for each different job.
```
select AVG(Sal), Job from Emp group by Job;
```

Q16) Display the minimum, maximum and average salaries for each job group.
```
select Min(Sal), Max(Sal), AVG(Sal), Job from Emp group by Job;
```

Q17) Find all departments which have less than three employee.
```
select Job from Emp group by Job having count(Job)<3;
```

Q18) List the details of the employee an ascending order of department no and within each department in descending order of salary.
```
select * from Emp order by Job, Sal desc;
```

Q19) Display the name, deptno and annual salary of each employee in order of salary and deptno.
```
select Ename, Deptno, Sal from Emp order by Sal, Deptno;
```