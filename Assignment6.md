This Assignment uses the Table made in Assignment 1

Q1) Display the name of employees who earned maximum salary.
```
select Ename from Emp where Sal=(select Max(Sal) from Emp);
```

Q2) Display the name of employees who earned minimum salary.
```
select Ename from Emp where Sal=(select Min(Sal) from Emp);
```

Q3) Display the name of employees who earned minimum salary whose job is clerk.
```
select Ename from Emp where Sal=(select Min(Sal) from Emp where Job='Clerk');
```

Q4) Display the name of employees who earned maximum salary whose job is salesman.
```
select Ename from Emp where Sal=(select Max(Sal) from Emp where Job='Salesman');
```

Q5) Display the department number whose average salary is maximum.
```
select Deptno from Emp group by Deptno having AVG(Sal)=(select Max(AVG(Sal)) from Emp group by Deptno);
```

Q6) List the name of the employee who works in the same department as Smith.
```
select Ename from Emp where Deptno=(select Deptno from Emp where Ename='Smith');
```

Q7) List the name of employees whose job is same as Clark.
```
select Ename from Emp where Job=(select Job from Emp where Ename='Clark');
```

Q8) List the name of the employees whose salary is more than Turner.
```
select Ename from Emp where Sal>(select Sal from Emp where Ename='Turner');
```

Q9) List the name the employees who joined after Allen.
```
select Ename from Emp where Hiredate>(select Hiredate from Emp where Ename='Allen');
```

Q10) List the name of the employee who joined in the same year as Adams.
```
select Ename from Emp where Extract(Year from Hiredate)=(select Extract(Year from Hiredate) from Emp where Ename='Adams');
```

Q11) List the name of the employee who joined in the same month of Blake.
```
select Ename from Emp where Extract(Month from Hiredate)=(select Extract(Month from Hiredate) from Emp where Ename='Blake');
```

Q12) List the name of the employee who joined in the same day of Adams.
```
select Ename from Emp where Extract(Day from Hiredate)=(select Extract(Day from Hiredate) from Emp where Ename='Adams');
```

Q13) List the name of department who gets commission.
```
select Job from Emp where Comm is not null group by Job;
```

Q14) List all employees who work in the same post as Smith.
```
select Ename from Emp where Job=(select Job from Emp where Ename='Smith');
```

Q15) List all employees who earn the lowest salary in their respective department.
```
select Ename from Emp where Sal = any (select Min(Sal) from Emp group by Deptno);
```

Q16) Find the job with the highest average salary.
```
select Job from Emp group by Job having AVG(Sal)=(select Max(AVG(Sal)) from Emp group by Job);
```