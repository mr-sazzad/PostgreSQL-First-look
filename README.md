## Hi There  👋

[![elephent Image](https://img.freepik.com/free-photo/animal-elephant-mammal-nature-wild-patterns-decoration-multi-colored-generative-ai_188544-9609.jpg?w=1060&t=st=1691409223~exp=1691409823~hmac=7c57826acbd142532d709b9241ec48db0eb3aceb6cf0728bfe7bf3c48075d854)](https://img.freepik.com/free-photo/animal-elephant-mammal-nature-wild-patterns-decoration-multi-colored-generative-ai_188544-9609.jpg?w=1060&t=st=1691409223~exp=1691409823~hmac=7c57826acbd142532d709b9241ec48db0eb3aceb6cf0728bfe7bf3c48075d854)

```css
 --## APPLY CONSTRAINTS
```

```sql
CREATE TABLE "user" (
    user_id SERIAL PRIMARY KEY,
    user_name VARCHAR(250) UNIQUE NOT NULL,
    email VARCHAR(50) UNIQUE NOT NULL,
    age INT DEFAULT 18
);
```
```css
 --##  INSART A COLUMN IN A TABLE
```

```sql
INSERT INTO table_name VALUES(1, 'xyz', 'xyz@gmail.com');
```

```css
 --## insert multipul column into a table
```

```sql
1. INSERT INTO table_name VALUES(1, 'xyz', 'xyz@gmail.com'),(2, 'abc', 'abc@gmail.com');
2. INSERT INTO table_name (user_name, email) VALUES ('sazzad', 'sazzad@gmail.com');
3. INSERT INTO table_name (user_id, user_name, email, age) VALUES (4, 'rakib', 'rakib@gmail.com', 40);
```

```css
--## retrieve all columns form table
```

```sql
SELECT * FROM Table_Name;
```

```css
--## DELETE a row from a table
```
 
 ```sql
DELETE FROM table_name WHERE user_id = 35;
```

```css
--## DELETE all rows without deleting the table
```


```sql
1. DELETE FROM table_name;
2. TRUNCATE TABLE table_name;
```

```css
 --## column queries

--## →→→ you shuld alwyes set a type when you create a column

--## add column
```

```sql
ALTER TABLE "user" ADD COLUMN password VARCHAR(30) NOT NULL;
ALTER TABLE "user" ADD COLUMN demo INT;
```

```css
--## drop column
```

```sql
ALTER TABLE "user" DROP COLUMN column_name;
```

```css
--## change data type
```

```sql
ALTER TABLE "user" ALTER COLUMN age FLOAT4;
```

```css
--## set default value
```

```sql
ALTER TABLE "user" ALTER COLUMN country set DEFAULT 'bangladesh';
```

```css
--## remove default value from a column
```

```sql
ALTER TABLE "user" ALTER COLUMN country DROP DEFAULT;
```

```css
--## rename a column
```

```sql
ALTER TABLE "user" RENAME COLUMN country to home;
```

```css
--## set constraints
```

```sql
ALTER TABLE "user" ALTER COLUMN set countrt NOT NULL;
```

```css
--## drop constraints
```


```sql
ALTER TABLE "user" ALTER COLUMN drop countrt;
```

```css
--## add constraints to a column
```


```sql
ALTER TABLE "user" ADD CONSTRAINTS unique_email UNIQUE(email);
```

```css
--## delete constraints from a column
```


```sql
ALTER TABLE "user" DROP CONSTRAINTS unique_email;
```

```css
-- Employee TABLE

-- Each employee belongs to a department
```

```sql
CREATE TABLE Employee(
    empID SERIAL PRIMARY KEY,
    empName VARCHAR(50) NOT NULL,
    departmentID INT,   --we use int because we don't need actually incremental id
    CONSTRAINT fk_constraint_dept
        FOREIGN KEY (departmentID)
        REFERENCES Department(deptID)
);
```

```css
 -- Department Table

-- Each Department has mny employees
```

```sql
CREATE TABLE Department(
    deptID SERIAL PRIMARY KEY,
    deptName VARCHAR(50) NOT NULL
);
```
```css
-- update database table row
```

```js
UPDATE Table
set
  ColumnName = ColumnValue
where courseID = 1;  --condition
```

```css
DELETE FROM TABLE
```

```js
DELETE FROM TableName 
WHERE condition = conditionValue;
```

```css
-- SELECT SOME COLUMN
```
```sql
SELECT name, email FROM TableName;
```

```css
-- EFFICIENT WAY FOR SEARCHING ALL COLUMN FROM A TABLE 👌
```
```sql
SELECT empid, name, email, salary, joiningdate, deptid FROM Table;
```

```sql
-- IF WE WANT TO VIEW JUST UNIQUE VALUES FROM A COLUMN


SELECT DISTINCT Column_Name FROM Table_Name
```
