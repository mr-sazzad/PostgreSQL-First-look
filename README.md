## Hi There  👋

[![elephent Image](https://img.freepik.com/free-photo/animal-elephant-mammal-nature-wild-patterns-decoration-multi-colored-generative-ai_188544-9609.jpg?w=1060&t=st=1691409223~exp=1691409823~hmac=7c57826acbd142532d709b9241ec48db0eb3aceb6cf0728bfe7bf3c48075d854)](https://img.freepik.com/free-photo/animal-elephant-mammal-nature-wild-patterns-decoration-multi-colored-generative-ai_188544-9609.jpg?w=1060&t=st=1691409223~exp=1691409823~hmac=7c57826acbd142532d709b9241ec48db0eb3aceb6cf0728bfe7bf3c48075d854)


> --## APPLY CONSTRAINTS

---
```sql
CREATE TABLE "user" (
    user_id SERIAL PRIMARY KEY,
    user_name VARCHAR(250) UNIQUE NOT NULL,
    email VARCHAR(50) UNIQUE NOT NULL,
    age INT DEFAULT 18
);
```

> --##  INSART A COLUMN IN A TABLE

---
```sql
INSERT INTO table_name VALUES(1, 'xyz', 'xyz@gmail.com');
```

> --## insert multipul column into a table

---
```sql
1. INSERT INTO table_name VALUES(1, 'xyz', 'xyz@gmail.com'),(2, 'abc', 'abc@gmail.com');
2. INSERT INTO table_name (user_name, email) VALUES ('sazzad', 'sazzad@gmail.com');
3. INSERT INTO table_name (user_id, user_name, email, age) VALUES (4, 'rakib', 'rakib@gmail.com', 40);
```

> --## retrieve all columns form table

---
```sql
SELECT * FROM Table_Name;
```

> --## DELETE a row from a table
 
 ---
 ```sql
DELETE FROM table_name WHERE user_id = 35;
```

> --## DELETE all rows without deleting the table

---
```sql
1. DELETE FROM table_name;
2. TRUNCATE TABLE table_name;
```

> --## column queries

> --## →→→ you shuld alwyes set a type when you create a column
> 
> --## add column

---
```sql
ALTER TABLE "user" ADD COLUMN password VARCHAR(30) NOT NULL;
ALTER TABLE "user" ADD COLUMN demo INT;
```

> --## drop column

---
```sql
ALTER TABLE "user" DROP COLUMN column_name;
```

> --## change data type

---
```sql
ALTER TABLE "user" ALTER COLUMN age FLOAT4;
```

> --## set default value

---
```sql
ALTER TABLE "user" ALTER COLUMN country set DEFAULT 'bangladesh';
```

> --## remove default value from a column

---
```sql
ALTER TABLE "user" ALTER COLUMN country DROP DEFAULT;
```

> --## rename a column

---
```sql
ALTER TABLE "user" RENAME COLUMN country to home;
```

> --## set constraints

---
```sql
ALTER TABLE "user" ALTER COLUMN set countrt NOT NULL;
```

> --## drop constraints

---
```sql
ALTER TABLE "user" ALTER COLUMN drop countrt;
```

> --## add constraints to a column

---
```sql
ALTER TABLE "user" ADD CONSTRAINTS unique_email UNIQUE(email);
```

> --## delete constraints from a column

---
```sql
ALTER TABLE "user" DROP CONSTRAINTS unique_email;
```

> -- Employee TABLE
> 
> -- Each employee belongs to a department

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

> -- Department Table
> 
> -- Each Department has mny employees

```sql
CREATE TABLE Department(
    deptID SERIAL PRIMARY KEY,
    deptName VARCHAR(50) NOT NULL
);
```
