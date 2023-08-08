## Hi There  👋

[![PostgreSQL Image](https://kinsta.com/wp-content/uploads/2022/02/postgres-logo.png)](https://github.com/mr-sazzad)


```sql
 -- APPLY CONSTRAINTS

CREATE TABLE "user" (
    user_id SERIAL PRIMARY KEY,
    user_name VARCHAR(250) UNIQUE NOT NULL,
    email VARCHAR(50) UNIQUE NOT NULL,
    age INT DEFAULT 18
);


 --  INSART A COLUMN IN A TABLE

INSERT INTO table_name VALUES(1, 'xyz', 'xyz@gmail.com');


 -- INSART MULTIPULE COLUMN TO A TABLE

1. INSERT INTO table_name VALUES(1, 'xyz', 'xyz@gmail.com'),(2, 'abc', 'abc@gmail.com');
2. INSERT INTO table_name (user_name, email) VALUES ('sazzad', 'sazzad@gmail.com');
3. INSERT INTO table_name (user_id, user_name, email, age) VALUES (4, 'rakib', 'rakib@gmail.com', 40);


-- RETRIEVE ALL COLUMN FROM A TABLE 🎉

SELECT * FROM Table_Name;


-- DELETE A ROW FROM A TABLE USING CONDITION 💎

DELETE FROM table_name WHERE user_id = 35;


-- DELETE all rows without deleting the table 💥

1. DELETE FROM table_name;
2. TRUNCATE TABLE table_name;
```

```sql
 -- COLUMN CUERIES
-- →→→ you shuld alwyes set a type when you create a column
-- add column

ALTER TABLE "user" ADD COLUMN password VARCHAR(30) NOT NULL;
ALTER TABLE "user" ADD COLUMN demo INT;


-- DROP A COLUMN

ALTER TABLE "user" DROP COLUMN column_name;


-- CHANGE DATA TYPE OF A COLUMN

ALTER TABLE "user" ALTER COLUMN age FLOAT4;


-- SET DEFAULT VALUE TO A COLUMN

ALTER TABLE "user" ALTER COLUMN country set DEFAULT 'bangladesh';


-- REMOVE DAFAULT VALUE FROM A COLUMN 💥

ALTER TABLE "user" ALTER COLUMN country DROP DEFAULT;


-- RENAME A COLUMN

ALTER TABLE "user" RENAME COLUMN country to home;
```

```sql
-- CONSTRAINTS
-- SET CONSTRAINTS

ALTER TABLE "user" ALTER COLUMN set countrt NOT NULL;


-- DROP CONSTRAINTS

ALTER TABLE "user" ALTER COLUMN drop countrt;


-- ADD CONSTRAINTS TO A COLUMN

ALTER TABLE "user" ADD CONSTRAINTS unique_email UNIQUE(email);


-- DELETE CONSTRAINTS FROM A COLUMN

ALTER TABLE "user" DROP CONSTRAINTS unique_email;
```

```sql
-- EMPLOYEE TABLE
-- EACH EMPLOYEE BELONGS TO A DEPARTMENT

CREATE TABLE Employee(
    empID SERIAL PRIMARY KEY,
    empName VARCHAR(50) NOT NULL,
    departmentID INT,   --we use int because we don't need actually incremental id
    CONSTRAINT fk_constraint_dept
        FOREIGN KEY (departmentID)
        REFERENCES Department(deptID)
);


 -- DEPARTMENT TABLE 
-- EACH DEPARTMENT HAS MANY EMPLOYEES
CREATE TABLE Department(
    deptID SERIAL PRIMARY KEY,
    deptName VARCHAR(50) NOT NULL
);
```

```js
// UPDATE DATABASE TABLE ROW 🎈

UPDATE Table
set
  ColumnName = ColumnValue
where courseID = 1;  --condition


// DELETE A ROW FROM A TABLE⛔

DELETE FROM TableName 
WHERE condition = conditionValue;
```

```sql
-- SELECT SOME COLUMN 🥗

SELECT name, email FROM TableName;


-- EFFICIENT WAY FOR SEARCHING ALL COLUMN FROM A TABLE 👌

SELECT empid, name, email, salary, joiningdate, deptid FROM Table;


-- IF WE WANT TO VIEW JUST UNIQUE VALUES FROM A COLUMN WE CAN USE "DISTINCT" 😎

SELECT DISTINCT Column_Name FROM Table_Name


-- FILTERING THOSE ROWS WHICH SATISFY THE CONDITION

1. SELECT * FROM Table_name WHERE salary > 30000;
2. SELECT * FROM Employee WHERE joining_date < '2020-01-1';


-- FILTERING THOSE ROWS WHICH SATISFY ATLEAST ONE CONDITION

SELECT * FROM Table_name WHERE salary < 50000 OR salary > 90000;


-- FILTERING THOSE ROWS WHICH NOT === TO THIS DATE 🥱

SELECT * FROM Employee WHERE joining_date <> '2020-01-1';
```
