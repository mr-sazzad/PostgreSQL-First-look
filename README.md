## Hi There  👋

[![elephent Image](https://img.freepik.com/free-photo/animal-elephant-mammal-nature-wild-patterns-decoration-multi-colored-generative-ai_188544-9609.jpg?w=1060&t=st=1691409223~exp=1691409823~hmac=7c57826acbd142532d709b9241ec48db0eb3aceb6cf0728bfe7bf3c48075d854)](https://img.freepik.com/free-photo/animal-elephant-mammal-nature-wild-patterns-decoration-multi-colored-generative-ai_188544-9609.jpg?w=1060&t=st=1691409223~exp=1691409823~hmac=7c57826acbd142532d709b9241ec48db0eb3aceb6cf0728bfe7bf3c48075d854)


```sql
 -- APPLY CONSTRAINTS

CREATE TABLE "user" (
    user_id SERIAL PRIMARY KEY,
    user_name VARCHAR(250) UNIQUE NOT NULL,
    email VARCHAR(50) UNIQUE NOT NULL,
    age INT DEFAULT 18
);
```

```sql
 --  INSART A COLUMN IN A TABLE

INSERT INTO table_name VALUES(1, 'xyz', 'xyz@gmail.com');
```


```sql
 -- insert multipul column into a table

1. INSERT INTO table_name VALUES(1, 'xyz', 'xyz@gmail.com'),(2, 'abc', 'abc@gmail.com');
2. INSERT INTO table_name (user_name, email) VALUES ('sazzad', 'sazzad@gmail.com');
3. INSERT INTO table_name (user_id, user_name, email, age) VALUES (4, 'rakib', 'rakib@gmail.com', 40);
```

```sql
-- retrieve all columns form table 🎉

SELECT * FROM Table_Name;
```

 
 ```sql
-- DELETE a row from a table

DELETE FROM table_name WHERE user_id = 35;
```



```sql
-- DELETE all rows without deleting the table 💥

1. DELETE FROM table_name;
2. TRUNCATE TABLE table_name;
```

```sql
 -- column queries
-- →→→ you shuld alwyes set a type when you create a column
-- add column

ALTER TABLE "user" ADD COLUMN password VARCHAR(30) NOT NULL;
ALTER TABLE "user" ADD COLUMN demo INT;
```



```sql
-- drop column

ALTER TABLE "user" DROP COLUMN column_name;
```

```sql
-- change data type

ALTER TABLE "user" ALTER COLUMN age FLOAT4;
```

```sql
-- set default value

ALTER TABLE "user" ALTER COLUMN country set DEFAULT 'bangladesh';
```

```sql
-- remove default value from a column 💥

ALTER TABLE "user" ALTER COLUMN country DROP DEFAULT;
```

```sql
-- rename a column

ALTER TABLE "user" RENAME COLUMN country to home;
```

```sql
-- set constraints

ALTER TABLE "user" ALTER COLUMN set countrt NOT NULL;
```

```sql
-- drop constraints

ALTER TABLE "user" ALTER COLUMN drop countrt;
```


```sql
-- add constraints to a column

ALTER TABLE "user" ADD CONSTRAINTS unique_email UNIQUE(email);
```



```sql
-- delete constraints from a column

ALTER TABLE "user" DROP CONSTRAINTS unique_email;
```

```sql
-- Employee TABLE
-- Each employee belongs to a department

CREATE TABLE Employee(
    empID SERIAL PRIMARY KEY,
    empName VARCHAR(50) NOT NULL,
    departmentID INT,   --we use int because we don't need actually incremental id
    CONSTRAINT fk_constraint_dept
        FOREIGN KEY (departmentID)
        REFERENCES Department(deptID)
);
```


```sql
 -- Department Table
-- Each Department has mny employees

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
```

```js
// DELETE A ROW FROM A TABLE⛔

DELETE FROM TableName 
WHERE condition = conditionValue;
```


```sql
-- SELECT SOME COLUMN 🥗

SELECT name, email FROM TableName;
```



```sql
-- EFFICIENT WAY FOR SEARCHING ALL COLUMN FROM A TABLE 👌

SELECT empid, name, email, salary, joiningdate, deptid FROM Table;
```

```sql
-- IF WE WANT TO VIEW JUST UNIQUE VALUES FROM A COLUMN WE CAN USE "DISTINCT" 😎


SELECT DISTINCT Column_Name FROM Table_Name
```
