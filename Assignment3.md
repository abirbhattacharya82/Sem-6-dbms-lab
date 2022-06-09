We will be Using The Table made in Assignment 1 for this Assignment

Q1) List the employee name starts with S.
```
select Ename from Emp where Ename like 'S%';
```

Q2) List all employees whose names start with A
```
select Ename from Emp where Ename like 'A%';
```

Q3) List all employees whose names end with N.
```
select Ename from Emp where Ename like '%n';
```

Q4) List the names and job of all employees who have names exactly 5 characters in length.
```
select Ename, Job from Emp where length(Ename)=5;
```

Q5) List the names and job of all employees who have names exactly 5 characters in length and ends with ‘S’.
```
select Ename, Job from Emp where length(Ename)=5 and Ename like '%s';
```

Q6) List all employees who have not joined between 1/1/81 and 31/12/81.
```
select Ename from Emp where Hiredate not between '1-Jan-81' and '31-Dec-81';
```

Q7) List all employees whose job does not start with ‘CL’.
```
select Ename from Emp where Job not like 'Cl%';
```

Q8) List all managers who earned more than Rs-4000.
```
select Ename from Emp where Job='Manager' and Sal>4000;
```

Q9) List all clerks and salesman who earned more than Rs-500.
```
select Ename from Emp where Job = 'Clerk' or Job = 'Salesman' and Sal>500;
```

Q10) List the names and salaries of all employees who were joined as manager during 1981.
```
select Ename, Sal from Emp where Job='Manager' and Hiredate like '%81';
```