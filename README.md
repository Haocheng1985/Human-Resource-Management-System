# Human-Resource-Management-System

##1. Project Function
Add/update/delete employee

Query all employees/ query employee by id

##2. Techniques
1. Access database using JDBC
2. Layered architecture<br>
    a.frontend: call backend function<br>
    b.backend: access database to return results
    
3. Code reuse by using class DBUtil
4. Access property file by using class Properties
5. Use Log4j to output log file
6. Extension: use reflection to query.


##3. Framework    
1. Create a project
2. Add jar packages: ojdbc8.jar and log4j-1.2.17.jar
3. Create packages:<br>
    a. com.luke.hrms.dao backend:interface for database<br>
    b. com.luke.hrms.dao.impl backend:implementation of accessing database<br>
    c. com.luke.hrms.service backend:interface for functions <br>
    d. com.luke.hrms.serviceImpl backend:implementation of functions <br>
    e. com.luke.hrms.test frontend: main() program<br>
    f. com.luke.hrms.util back:class DBUtil for connecting database(oracle)<br>
    g. com.luke.hrms.pojo class for employee
4. Create class Employee
5. create interface class and implementation class<br>
    a. com.luke.hrms.pojo.Emp :employee class<br>
    b. com.luke.hrms.util.JdbcUtil : connect database<br>
    c. com.luke.hrms.dao.impl.EmpDaoImpl :backend service<br>
    d. com.luke.hrms.serviceImpl.EmpServiceImpl :business tier<br>
    e. com.luke.hrms.test.Test :front end service to terminal<br>
##4. Function lists
1. Query all employees
2. Query employee by id
3. Add employee
4. update employee's name
5. delete employee
6. exit

##5. Database design for table emp
EMPNO ENAME JOB MGR HIREDATE SAL COMM DEPTNO

##6. SQL statements
1.Query all employees:<br>
select * from emp<br>
2.Query employee by id:<br>
select * from emp where empno=?<br>
3.Add employee:<br>
insert into emp values(?,?,?,?,?,?,?,?)<>br
4.update employee's name:<br>
update emp set ename=? where empno=?<br>
5.delete employee:<br>
delete from emp where empno=?   


##
db.properties-->JdbcUtil-->EmpDaoImpl--->EmpServiceImpl-->Test

##
Notes From lookk

##
Notes From Haocheng 2020-5-1 11:27
