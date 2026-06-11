- [Database Management Systems](#"Database""Management""Systems")
- [MySQL Benefits](#"MySQL""Benefits")
- [ER Diagrams](#"ER""Diagrams")
- [SQL Commands](#"SQL""Commands")
  - [Database Operations](#"Database""Operations")
  - [Table Operations](#"Table""Operations")
    - [Example Creating A Table](#"Example""Creating""A""Table")
    - [Example Inserting Data](#"Example""Inserting""Data")
    - [Example Creating Foreign Key](#"Example""Creating""Foreign""Key")
  - [Select Operations In Table](#"Select""Operations""In""Table")
    - [Example For Select](#"Example""For""Select")
    - [Example Underscore For Select](#"Example""Underscore""For""Select")
  - [Delete Truncate And Drop](#"Delete""Truncate""And""Drop")
  - [Update And Alter](#"Update""And""Alter")
  - [Alter](#"Alter")
    - [Add](#"Add")
    - [Modify](#"Modify")
    - [Drop](#"Drop")
    - [Rename](#"Rename")
  - [Aggregation](#"Aggregation")
  - [Operators](#"Operators")
    - [Boolean Operators](#"Boolean""Operators")
    - [Between Operator](#"Between""Operator")
    - [In Operator](#"In""Operator")
    - [Is Operator](#"Is""Operator")
  - [Clause](#"Clause")
    - [From](#"From")
    - [Where](#"Where")
    - [Order By](#"Order""By")
    - [Limit](#"Limit")
    - [Top](#"Top")
    - [Group By](#"Group""By")
    - [Having](#"Having")
  - [Joins](#"Joins")

## Database Management Systems
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
## ER Diagrams

*Note: The original text referenced ![[Pasted image 20260603163734.png]]

- **Primary Key:** Uniquely identifies a record in a table. Every entity must have one primary key.
- **Attributes:** The specific properties or traits that describe an entity (e.g., a "Product" entity has attributes like *price*, *name*, and *stock*). 
- **Foreign Key:** A field used to establish and maintain a relationship between two or more tables.

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

#### Example Creating A Table
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

#### Example Inserting Data
```sql
INSERT INTO product 
    (product_id, product_name, categories, sub_categories, original_price, selling_price, stock) 
VALUES 
    ('p101', 'television', 'electronics', 'sony', 25000, 21000, 10); 
```
#### Example Creating Foreign Key

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
### Select Operations In Table
#### Example For Select
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

#### Example Underscore For Select
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



### Delete Truncate And Drop

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

### Update And Alter

used to modify the existing data ;

```sql 
update employee set emp_name = 'jhaduwala' where emp_ID = 'e106';
-- updates the name of emp id e106 to 'jhaduwala'
```
![[Pasted image 20260605163710.png]]

### Alter

used to modify and do changes in columns , table 

#### Add
```sql
alter table employee add email varchar(50) not null;
```
![[Pasted image 20260605164128.png]]


```sql 
alter table employee_details add constraint primary key (emp_ID);
--adding primary key 
```

![[Pasted image 20260605165729.png]]

#### Modify
```sql 
alter table employee modify email varchar(60) not null;
```

![[Pasted image 20260605164241.png]]

#### Drop
```sql 
alter table employee drop column email;
```
![[Pasted image 20260605164351.png]]

```sql 
alter table employee_details drop primary key;
--Drop the primary key
```

![[Pasted image 20260605165519.png]]


#### Rename
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

### Aggregation

**aggregation** means **combining multiple rows of data into a single summarized value**.

5 functions
1. sum()  ⇒ value of submission 

```sql 
select sum(Total_price) from orderdetails;
```
![[Pasted image 20260608164418.png]]

2. avg()=> average

```sql 
select avg(Total_price) from orderdetails;
```
![[Pasted image 20260608164605.png]]

3. count () ⇒ used to count number of rows in the set 

```sql 
select count(*) from orderdetails; 
```
![[Pasted image 20260608164834.png]]

4. max()=> returns the maximum value out of the set 
```sql
select max(quantity) from orderdetails;
```
![[Pasted image 20260608165019.png]]

5. min()=> returns the minimum value out of the set 
```sql 
select min(quantity) from orderdetails;
```


### Operators
#### Boolean Operators

and ⇒  if both condition are true then the condition is valid
```sQL
select * from orderdetails where quantity=10 and Order_status='shipped';
```
![[Pasted image 20260608165857.png]]

or ⇒ if one of the condition is true the condition is valid
```sql
select * from orderdetails where quantity=10 or Order_status='pending'; 
```
![[Pasted image 20260608170100.png]]

#### Between Operator
to filter the data within a specific range 

.value must be from minimum to maximum
  
```sql
select * from orderdetails where Order_Id between 'o101' and 'o103';
```
![[Pasted image 20260608170902.png]]

not between
```sql 
select * from orderdetails where Order_date not between '2026-07-29' and '2026-08-01' ;
```
![[Pasted image 20260608171524.png]]

#### In Operator

 is used to specify the specific value , based on it we have to retrieve the data 
```sQL
select * from orderdetails where order_ID in ('o101','0103','o104');
```
![[Pasted image 20260608172338.png]]

not in 
opposite
```sql 
select * from orderdetails where quantity not in (20,5);
```
![[Pasted image 20260608172656.png]]

#### Is Operator
to check the null value is present in the database
```sql 
select * from orderdetails where quantity is null;
```
![[Pasted image 20260608173133.png]]

is not
```sql 
select * from orderdetails where quantity is not null;
```
![[Pasted image 20260608173203.png]]

---

### Clause

#### From
Used to retrieve (fetch) data from one or more tables in a database.
```sQL
SELECT * FROM employee;
```
#### Where
Used to filter  the rows  , before the grouping ,not in aggregation funciton
```sQL
SELECT * FROM employee
WHERE salary > 20000;
```
#### Order By
organise the data by ascending or descending order 
```sql 
select * from orderdetails order by quantity;
```
![[Pasted image 20260608173844.png]]

for descending 
```sql 
select * from orderdetails order by quantity desc; 
--desc at the end for making it descending 
```
![[Pasted image 20260608173949.png]]

#### Limit
(doesnt work in sql server database )
```sql 
select * from orderdetails limit 2 ;
```
![[Pasted image 20260608174439.png]]

#### Top
not included in mysql 

#### Group By
arrange the data in the group format , for grouping purpose always use the Aggregation function  , grouping the rows , 
```sql
select dept,count(*) as total_employee from employee group by dept;
```
![[Pasted image 20260609164610.png]]
```sql 
select dept,sum(salary) as total_salary from employee group by dept;
		-- to get the total salary of each dept 
```
![[Pasted image 20260609164940.png]]

#### Having
used to filter the group, after grouping ,always comes with group by , can be used in aggregation function 
```sQL
select dept,count(*) as total from employee group by dept having count(*) > 1;
		--value greater then one 
```
![[Pasted image 20260609170222.png]]
```SQL
select dept,sum(salary) as total from employee group by dept having sum(salary) > 10000;
-- salary more than 10000
```
![[Pasted image 20260609170701.png]]

---
### Joins
combine the rows from two or more tables  based on the related table 

inner joins , left joins ,  right outer join , full join , self join , cross join
![[Pasted image 20260610163053.png]]

1. inner joins.
   only returns the matching rows of the both table 

2. left join 
	returns all the rows of the left table and matching rows of the right table 

3.  right join 
	returns all the rows of the right table and matching rows of the left table 

4. full join 
	return all the rows from both table 

5. cross join represents the cartesian product 
	 every record is connected to the other table record 

6. self join 
	when one table connecting to itself is called the self join 

inner join 
```sQL
select emp_name, dept_name from employee inner join dept on employee.dept_id = dept.dept_id;
```
![[Pasted image 20260610165930.png]]

left join 
```sQL
select emp_name, dept_name from employee left join dept on employee.dept_id = dept.dept_id;
```
![[Pasted image 20260610170121.png]]

right join 
```sql 
select emp_name, dept_name from employee right join dept on employee.dept_id = dept.dept_id;
```
![[Pasted image 20260610170356.png]]

full join 
my sql does not support full outer join 
```sql 
select emp_name, dept_name from employee full join dept;
```
![[Pasted image 20260610170612.png]]

cross join 
```sql 
select emp_name, dept_name from employee cross join dept ;
```
![[Pasted image 20260610170720.png]]



---

