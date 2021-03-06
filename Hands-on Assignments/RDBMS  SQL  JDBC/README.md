# RDBMS / SQL / JDBC

#### **Oracle 11g Introduction**



**1.**

```
 Using SQL Developer: Create a database connection using the following information:
Connection Name: myconnection
Username: hr
Password: hr
Hostname: localhost
Port: 1521
SID: ORCL
Ensure that you select the Save Password check box.
Testing and Connecting Using the Oracle SQL Developer Database Connection
If the status is Success, connect to the database using this new connection.
```

**2.**

```
 Expand MyConnection -- > Explore
All the available table
structure of Employee table - its columns
view the data tab of the Employee tables
```

**3.**

```
 Start SQLPLUS
using UserName : hr
password : hr
```



#### **Select Statement**



**1.**

```
Determine the structure of the DEPARTMENTS table and its contents.
```

**2.**

```
Create a query to display the last name, job ID, hire date, and employee ID for each employee, with the employee ID appearing first. Provide an alias STARTDATE for the HIRE_DATE column.
```

**3.**

```
 Create a query to display all unique job IDs from the EMPLOYEES table.
```

**4.**

```
Create a query to display employee id, last name, job id and hiredate from employee table with more describing column names.  Name the column headings 
Emp # , Employee , Job and Hire Date respectively.
```

**5.**

```
Create a report of all employees and their job IDs. Display the last name concatenated with the job ID (separated by a comma and space) and name the column as "Employee and Title"
```



#### **Restricting and Sorting Data**



**1.**

```
Create a report that displays the last name and salary of employees who earn more than $12,000.
```

**2.**

```
 Create a report that displays the last name and department number for employee number 176.
```

**3.**

```
To find high-salary and low-salary employees. Create a query to display the last name and salary for any employee whose salary is not in the range of $5,000 to $12,000
```

**4.**

```
 Create a report to display the last name, job ID, and hire date for employees with the last names of Matos and Taylor. Order the query in ascending order by the hire date.
```

**5.**

```
 Display the last name and department ID of all employees in departments 20 or 50 in ascending alphabetical order by name.
```

**6.**

```
List employees who earn between $5,000 and $12,000, and are in department 20 or 50. Label the columns as
Employee and Monthly Salary, respectively.
```

**7.**

```
` Create a report that displays the last name and hire date for all employees who were hired in 1994.`
```

**8.**

```
 Create a report to display the last name and job title of all employees who do not have a manager.
```

**9.**

```
 Create a report to display the last name, salary, and commission of all employees who earn commissions. 
Sort data in descending order based on salary and commissions. Use the column???s numeric position in the ORDER BY clause.
```

**10.**

```
 Create a report that displays the last name and salary of employees who earn more than an amount that the user specifies after a prompt. 
If you enter 12000, it should display all employees earning more than 12000.
Eg: Salary_value: 12000
```

**11.**

```
 Create a query that prompts the user for a manager ID and generates the employee ID, last name, salary and department for that manager???s employees and
prompts a column name by which result should be sorted.
Eg:
manager_id :103
sorted_by : last_name
```

**12.**

```
 Display all employee last names in which the third letter of the name is ???a???.
```

**13.**

```
 Display the last names of all employees who have both an ???a??? and an ???e??? in their last name.
```

**14.**

```
 Display the last name, job, and salary for all employees whose jobs are either those of a sales representative or of a stock clerk, and whose salaries are not equal to $2,500, $3,500, or $7,000.
```



#### **DML**



**1.**

```
 Run the below script
Create table MY_EMPLOYEE 
as
Select employee_id,first_name,last_name,department_id,salary from EMPLOYEES where 1=2;
```

**2.**

```
 Test the table creation by viewing the structure using describe command

Name                           Null     Type                                                                                                                                                                                          
------------------------------ -------- ------------------------------
EMPLOYEE_ID                             NUMBER(6)                                                                                                                                                                                     
FIRST_NAME                              VARCHAR2(20)                                                                                                                                                                                  
LAST_NAME                      NOT NULL VARCHAR2(25)                                                                                                                                                                                  
DEPARTMENT_ID                           NUMBER(4)                                                                                                                                                                                     
SALARY                                  NUMBER(8,2)                                                                                                                                                                                   
5 rows selected
```

**3.**

```
Insert one record without listing the column names in the insert statement. Check whether data is inserted
Eg:
employee_id    first_name    last_name    department_id     salary
201             Michael       Hartstein      20          13000
```

**4.**

```
 Insert one record without listing the column names in the insert statement where salary value remain undetermined. Check whether data is inserted
Eg: 
employee_id first_name last_name  department_id salary
201         Michael     Hartstein   20         13000
202         Pat            Fay       20         (null)
```

**5.**

```
 Insert one record with listing the column names avoiding salary column in the insert statement where salary value remain undetermined. Check whether data is inserted
employee_id first_name last_name department_id salary
201       Michael        Hartstein   20          13000
202       Pat             Fay          20         (null)
203       Susan           Mavris        40        (null)
```

**6.**

```
 Use the above Script to insert the below given records
employee_id first_name last_name department_id salary
205        Shelley        Higgins       110      12000
100        Steven         King            90       24000
101        Neena          Kochhar       90         17000
102        Lex De         Haan            90       17000
111        Ismael         Sciarra        100        7700
112        Jose Manuel    Urman         100        7800
204        Hermann        Baer           70       10000
```

**7.**

```
 Create a query to increase salary by 10% for all employees in dept 90.
```

**8.**

```
 Create a query to update Last_name of emp 202 to Higgins.
```

**9.**

```
Delete employees whose name either first or last name has char seq of ???man???
```



#### **DDL**



**1.**

```
 Create the DEPT table based on the following table instance chart. Save the statement in a script called lab_10_01.sql , and then execute the statement in the script to create the table. Confirm that the table is created.
Specification Values:
Column named Dept_ID of Numeric 7 size and would be a primary key.
Column named Dept_Name of varchar2 size 20.
```

**2.**

```
Populate the DEPT table with data from the DEPARTMENTS table. Include only columns that you need.
Insert dept Id 10 and Name Accounts
Insert dept Id as null and Name as TT
Correct by giving 20 and TT
Insert A1 as Id and Accounts
Correct by giving 30 and Accounts
```

**3.**

```
 Create the EMP table based on the following table instance chart. Save the statement in a script called lab_10_03.sql , and then execute the statement in the script to create the table. Confirm that the table is created.
Specification-  Values
Column Name: ID, LAST_NAME, FIRST_NAME, DEPT_ID
Key Type: PK,  -,  -, FK
Nulls /Unique:  -,  Not null,  -,  -,
FK Table:   -,  -,    -, Dept
FK Column:   -,   -,  -,  ID
Data type: NUMBER, VARCHAR2, VARCHAR2, NUMBER
Length: 7, 25, 25, 7

Insert 101,Sam,Sundar,10
Insert 101,Ram,Krishna,20
Insert 102,Gopi,null,40
Insert 103,null,ram,20
```



#### **Establishing Connection**



**1.**

```
 Write a java program that establishes a connection to oracle database successfully. If the connection is successful, it should display a message ???Connection Established successfully???. In case, it is not able to do so due to any exception, it should display the message ???Connection could  not be established ???. If there is an exception, it should also display the description of the exception.
```

**2.**

```
In the just concluded exercise, where you have established the connection successfully, exclude the registration process(by commenting the line containing the code Class.forName(???..???)). Observe the result.
```



#### **Executing Query & Processing Results**



**1.**

```
 Write a java program that connects to oracle database, queries the inbuilt table ???emp??? and displays the first two columns (empno using column index and ename using column name ) of all the rows.
```

**2.**

```
 Modify the above program to display all the rows where sal is greater than 1000 and less than 2000. Display the columns ename, job, sal and comm.
```



#### **Using PreparedStatement & MetaData objects**



**1.**

```
 Develop a jdbc program containing main method, which should instantiate a class called DAOClass, which should contain methods called insert, delete, modify and display. Description of what each of these methods are expected to do is given below. Necessary details required for executing these methods, are passed from command line argument. For e.g. If the name of the class containing the main method is JDBCCalls, then if you want to insert a record, you will execute this class as java JDBCCalls 1 101 ???Ajit??? ???IV??? ???20-Nov-2001??? 4000
Where 1 is the option for inserting the record and all other details are the values for the columns in each row of the student table. The structure of student table is given below. Similarly, for deleting a record, you have to execute the code as 
java JDBCCalls 2 101
where 2 is the option for deleting a record and 101 is the rollno of the student, whose record has to be deleted.
For modifying a record, you will use
java JDBCCalls 3 101 4500, where 3 is the option for modifying a record and the 4500 is the new fee which needs to replace the old fee value.
For Displaying records, if the main class is executed as follows 
java JDBCCalls 4 101
it should display only one record, that of the student with roll no. 101. 4 option is for displaying the record. 
If the main class is executed as
java JDBCCalls 4 (without specifying the rollno.), it means that details of all the students should be displayed.
```

**2.**

```
 Inserting a record
ABC International School wants to computerize students details. The school maintains a database of students in Oracle. The student table contains information related to students and is shown in the following student table structure. 
Column Name Type  Constraint
Rollno Number (4) Primary Key
StudentName Varchar (20)  Not Null
Standard Varchar (2) Not Null
Date_Of_Birth Date 
Fees Number (9,2) 
           
 When a new student joins the school, the student record is inserted in the student table.  The valid student details are as follows:
??? Rollno: Valid value is a 4-digit number 
??? StudentName: Valid value can contain maximum 20 letters in uppercase
??? Standard : Valid values are Roman Letters representing I to X(I, II, III, IV???.IX, X)
Write a Java program to insert some records to the table
```

**3.**

```
Deleting a Student???s record
When a student leaves the school, the record related to that student needs to be deleted from the Student table. The student???s roll no, whose record has to be deleted, should be passed as a command line argument.
Upon deletion, the Student details must be stored in another table named StudentLog which will maintain the details such as Rollno, StudentName, Standard and Leaving_date.
```

**4.**

```
 Modification of Student record 
When there is a change in the fee to be paid by a student, the respective row should be appropriately updated. Pass the rollno from the command prompt along with the new fee amount and this amount should be reflected in the table for that particular student.
```

**5.**

```
 Display Student details
Write the code to display details of all the students, if no roll no. is passed, while executing the main program.
If while executing the main program, the roll no. is passed, then it should display the record of that particular student.
```



####  **Using CallableStatement and Transactions**



**1.**

```
 Create a stored procedure that calculates net salary of all the employees whose records are stored in table "emp".
The criteria for calculating net salary is as follows :
Gross salary = sal + comm.
Net Salary = gross salary - IT
If the employee's commission is null then IT is calculated as
IT =  10% of gross salary
else if the employees commission is less than 500, then IT is calculated as
IT =  15% of gross salary
else
IT = 20% of gross salary.
Develop a jdbc program that invokes this stored procedure by passing the empno. and in return gets the net salary of each employee. Display on screen the empno., ename and net salary of all the employees.
```