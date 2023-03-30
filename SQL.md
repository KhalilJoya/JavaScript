# MySQL

### 1. khan

```
select * from students where name like '%Khan%';
```

### 2. where studentid between 5 and 10

```
select * from students where studentid between 5 and 10;
```

### 3. Rename fathername column to mothername

```
ALTER TABLE students RENAME COLUMN fathername TO MotherName;
```

### 4. kaunse month me sbse jyada fees aayi hai

```
select month, sum(amount) as total from fees group by month order by total desc limit 1;
```

### 5. kaunse month me sbse kam fees aayi hai

```
select month, sum(amount) as total from fees group by month order by total asc limit 1;
```

### 6. sbse jyada fees kis student ne di hai

```
select StudentFeesid, sum(amount) as total from fees group by StudentFeesid order by total desc limit 1;
select * from students where studentid = 1;
```

### 7. sbse kam fees kis student ne di hai

```
select StudentFeesid, sum(amount) as total from fees group by StudentFeesid order by total asc limit 1;
select * from students where studentid = 9;
```

### 8. aise kaunse student hai jinhone ek b bar fee ni di hai

```
select distinct StudentFeesid from fees;
select * from students where studentid not in (21,22,23);
```

### 9. aise kaunse students hai jinka mobile and fathername ni hai db me

```
select * from students where mobile is null and fathername is null
```

### 10. vo sare students ka record delete krdo jinhone koi fees ni di hai

```
select distinct StudentFeesid from fee;
delete from students where studentid not in (24,25);
```

### 11. Create Database

```
create database wecodeacademy;
```

### 12. Show Databases

```
Show Databases
```

### 13. Select Database

```
use wecodeacademy;
```

### 14. Create Table

```
CREATE TABLE `student` (
 `studentid` int(10) UNSIGNED PRIMARY KEY NOT NULL AUTO_INCREMENT,
 `name` varchar(255) ,
 `email_address` varchar(255),
 `city` varchar(255) ,
 `fathername` varchar(255),
 `mobile` bigint
);
```

### 15. Show Tables

```
show tables;
```

### 16. Select All Columns from a table

```
select * from student;
```

### 17. Select specific columns from a table

```
select name, mobile from student;
```

### 18. Insert into table using column names

```
INSERT INTO student (name, email_address, city, fathername, mobile) ;
VALUES (1, 'Khalil Jooya' ,'Khalil@gmail.com', 'Merta', 'Murad Kha Joya',  9079883575);
```

### 19. Insert into table without using column names

```
INSERT INTO student VALUES (1, 'Khalil Jooya' ,'Khalil@gmail.com', 'Merta', 'Murad Kha Joya',  9079883575);
```

### 20. Where Condition examples

```
select * from student where name  = 'Sajid' or studentid  = 2;
select * from student where name  = 'Sajid' and studentid  = 2;
```

### 21. distinct

```
select distinct name from student;
```

### 22. How to create the student table in MySQL?

```
CREATE TABLE `students`(
    studentid int(10) UNSIGNED PRIMARY KEY NOT NULL AUTO_INCREMENT,
     name varchar(255) ,
     email_address varchar(255),
     city varchar(255) ,
     fathername varchar(255),
     mobile bigint
      );
```

### 23. How to create the fees table in MySQL?

```
CREATE TABLE `fees` (
    feeid integer UNSIGNED PRIMARY KEY NOT NULL AUTO_INCREMENT,
    amount bigint, month varchar(255),
    studentid int unsigned,
    CONSTRAINT FK_StudentId FOREIGN KEY (studentid) ,
    REFERENCES Student(studentid)
     );
```

### 24. How to insert a new fee record into the fees table for a particular student?

```
INSERT INTO fee (amount, month, studentid);
 VALUES (5000 ,'Jan', 1);
```

### 25. How to update a student record in the student table?

```
update students set fieldname = value, field2=value where studentid = ?;
```

### 26. How to update a fee record in the fees table?

```
update fee set fieldname = value, field2=value where studentid = ?;
```

### 27. How to select all the records from the fees table?

```
select * from fee;
```

### 28. How to select a particular student record from the student table?

```
select * from student where condition;
```

### 29. How to select all the fee records for a particular student from the fees table?

```
select * from fee where studentid = ?;
```

### 30. How to get the total number of students in the student table?

```
select count(*) from student;
```

### 31. How to get the sum of all the fees paid by a particular student?

```
select sum(amount) from fee where studentid = ?;
```

### 32. How to get the average fee paid by all the students?

```
select avg(amount) from fee;
```

### 33. How to get the student record with the highest mobile number in the student table?

```
select max(mobile) from student;
```

### 34. How to get the fee record with the highest fee amount in the fees table?

```
select max(amount) from fee;
```

### 35. How to get the list of all students who live in a city?

```
select * from student where city = ?;
```

### 36. How to get the list of all cities along with the count of students living in each city?

```
select city,count(studentid) from student group by city;
```

### 37. How to get the list of all cities along with the count of students living in each city, where the count is greater than 1?

```
select city,count(studentid) as total from student group by city having total > 1;
```

### 38. How to get the list of all students sorted by their names in ascending order?

```
SELECT * FROM students ORDER BY studentsName;
SELECT * FROM students ORDER BY studentsName ASC;
```

### 39. How to get the list of all students sorted by their mobile numbers in descending order?

```
select * from student order by mobile desc;
```

### 40. How to get the list of all fees records sorted by the fee amount in descending order?

```
select * from fee order by amount desc;
```

### 41. How to get the list of all fees records sorted by the fee amount in descending order, for a particular student?

```
select * from fee where studentid = ? order by amount desc;
```

### All Commmands

```
select count(*) from student;

select * from student where fathername is null;

select * from student where fathername is not null;

select * from student where studentid <> 5;

select * from student where studentid < 5;

select * from student where studentid > 5;

select * from student where studentid >= 5;

select * from student where studentid <= 5;

select * from student where studentid in (1,4,7,8,10);

select * from student where studentid not in (1,2,3);

select * from student where email_address like '%sher';

select * from student where email_address like '%er%';

select * from student where email_address like '%gmail.com';

select * from student where email_address like '%badnam%.com';

select * from student where studentid between 5 and 8;

select * from student order by name;

select * from student order by name asc;

select * from student order by name desc;

select * from student where not studentid = 2;

SET SQL_SAFE_UPDATES=0;

delete from student where Name = 'Shera';

delete from student;

drop table student;

drop database wecodeacademy;

select min(studentid) from student;

select max(name) from student;

select count(*) from student;

select count(studentid) from student;

select count(*) from student where fathername = 'Kalam Khan';

select avg(studentid) from student where fathername = 'Kalam Khan';

select sum(studentid) from student;
```
