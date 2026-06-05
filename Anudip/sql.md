# Database Management Systems (DBMS)
	
> [!summary] Core Concepts
> **DBMS** stands for Database Management System. Its core operations are based on **CRUD**:
> - **C**reate
> - **R**ead
> - **U**pdate
> - **D**elete
> 
> **Types of Databases:**
> 1. Relational (SQL)
> 2. Non-relational (NoSQL)
> 
> **SQL:** Structured Query Language

## MySQL Benefits
- **Cross-platform:** Runs on multiple operating systems.
- **Security:** High-level data protection and user access control.

> [!question] Interview Question: `CHAR` vs `VARCHAR`
> - **`CHAR`**: Fixed-length string. If the data is shorter than the defined length, it pads the rest with spaces.
> - **`VARCHAR`**: Variable-length string. The length adapts based on the specific requirement of the data entered, saving storage space.

---

## SQL Commands

*Note: The original text referenced 
![[Pasted image 20260602163825.png]] 


### Database Operations
```sql
SHOW DATABASES;          -- Shows all databases on the device
CREATE DATABASE db_name; -- Creates a new database
USE db_name;             -- Selects the specific database to use
```

### Table Operations
```sql
SHOW TABLES;               -- Shows all tables in the current database
DESC table_name;           -- Gives the description (schema) of the table
SELECT * FROM table_name;  -- Selects and displays all records from the table
```

#### Example: Creating a Table
```sql
CREATE TABLE product (
    product_id VARCHAR(10) NOT NULL PRIMARY KEY, 
    product_name VARCHAR(20) NOT NULL, 
    categories VARCHAR(30) NOT NULL, 
    sub_categories VARCHAR(30) NOT NULL, 
    original_price DOUBLE NOT NULL, 
    selling_price DOUBLE NOT NULL, 
    stock INT NOT NULL 
);
```

#### Example: Inserting Data
```sql
INSERT INTO product 
    (product_id, product_name, categories, sub_categories, original_price, selling_price, stock) 
VALUES 
    ('p101', 'television', 'electronics', 'sony', 25000, 21000, 10); 
```
#### Example : Creating Foreign key 

```sql
CREATE TABLE orderdetails (
    Order_Id VARCHAR(20) NOT NULL PRIMARY KEY,
    Customer_id VARCHAR(10) NOT NULL,
    product_id VARCHAR(10) NOT NULL,
    quantity DOUBLE NOT NULL,
    Total_price DOUBLE NOT NULL,
    Payment_mode VARCHAR(50) NOT NULL,
    Order_date DATETIME NOT NULL,
    Order_status VARCHAR(40) NOT NULL,

    FOREIGN KEY (Customer_id)
        REFERENCES customer(Customer_id),   //foreign key

    FOREIGN KEY (product_id)
        REFERENCES product(product_id)
);
```
### Select operations in table 
#### Example % for select 
for pattern matching

```sql 
-- Names starting with 'R'
SELECT * FROM customer
WHERE Name LIKE 'R%';

-- Names ending with 'R'
SELECT * FROM customer
WHERE Name LIKE '%R';

-- Names containing 'R' anywhere
SELECT * FROM customer
WHERE Name LIKE '%R%';
```

#### Example _  for select
one _  = 1 value
```sql 
-- City ends with 'i' (5 characters before i)
SELECT * FROM customer
WHERE city LIKE '_____i';

-- City has 'm' at 3rd position
SELECT * FROM customer
WHERE city LIKE '__m___';

-- Name pattern: m_n_s_
SELECT * FROM customer
WHERE name LIKE 'm_n_s_';

-- Exactly 4-letter names
SELECT * FROM customer
WHERE name LIKE '____';

-- Names starting with 'S' and 5 total letters
SELECT * FROM customer
WHERE name LIKE 'S____';

-- Names with 'a' in 2nd position and 5 letters total
SELECT * FROM customer
WHERE name LIKE '_a___';

-- Names with 's' in 4th position
SELECT * FROM customer
WHERE name LIKE '___s__';

-- Names containing pattern 'a' as 2nd and 'n' as 3rd
SELECT * FROM customer
WHERE name LIKE '_an___';


```



### Delete , truncate & drop 

1. Delete only remove records and not the whole structure of a particular database 
	u can remove specific rows

2. Truncate use to remove all the rows , does not remove the structure 

3. Drop used to remove the ENTIRE table  with structure 

```sql 
delete from student where student_id = 's102';
							--use primary key to be more precise
```

```sql 
truncate table student;
```

```sql 
drop table student;
```

### update & Alter

used to modify the existing data ;

```sql 
update employee set emp_name = 'jhaduwala' where emp_ID = 'e106';
-- updates the name of emp id e106 to 'jhaduwala'
```
![[Pasted image 20260605163710.png]]

### Alter

used to modify and do changes in columns , table 
### add
```sql
alter table employee add email varchar(50) not null;
```
![[Pasted image 20260605164128.png]]


```sql 
alter table employee_details add constraint primary key (emp_ID);
--adding primary key 
```

![[Pasted image 20260605165729.png]]

#### modify
```sql 
alter table employee modify email varchar(60) not null;
```

![[Pasted image 20260605164241.png]]

#### drop
```sql 
alter table employee drop column email;
```
![[Pasted image 20260605164351.png]]

```sql 
alter table employee_details drop primary key;
--Drop the primary key
```

![[Pasted image 20260605165519.png]]


#### rename 
```sql 
 alter table employee rename column email to emp_email, rename column phone to emp_phone;
```
![[Pasted image 20260605165021.png]]
```sql 
alter table employee rename to employee_details;
-- renamed the entire table
```
![[Pasted image 20260605165211.png]]


---

## ER Diagrams

*Note: The original text referenced ![[Pasted image 20260603163734.png]]

- **Primary Key:** Uniquely identifies a record in a table. Every entity must have one primary key.
- **Attributes:** The specific properties or traits that describe an entity (e.g., a "Product" entity has attributes like *price*, *name*, and *stock*). 
- **Foreign Key:** A field used to establish and maintain a relationship between two or more tables.



