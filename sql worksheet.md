# Queries

## Insert queries
```sql 

***ANSWER 

1. Insert a row with your name and all the other fields in **students** table


INSERT INTO instructors VALUES (7, 'A' , 'B' , 'email.com', 'phone');

INSERT INTO instructors VALUES (8, 'B','E','email','phone2');


INSERT INTO instructors VALUES( 10,'K JITHENDHAR', 'REDDY' , ' EMAIL', 83929);

INSERT INTO instructors VALUES (12,'ROCK', 'JOHN', 'rockjohn@gmail.com', 1234567);
 


```sql
    

2. Insert a row with just mandatory fields in **students** table
```sql

***ANSWER 
INSERT INTO `instructors` ( first_name , last_name , email) VALUES ( 'A','B','EMAIL');

    
```

---

## Select Queries
1. Get all students

    ```sql

    ***ANSWER 
     SELECT * FROM instructors;

     SELECT * FROM students;
    ***
    ```


2. Get first and last name of all students

    ```sql
    ***ANSWER 
    SELECT first_name , last_name FROM students;
    ```



3. Get first name of all students with output column name as `Student Name`
    
    ```sql
    ***ANSWER 
    SELECT first_name ,last_name AS 'FULL NAME ' FROM students;
    SELECT first_name AS 'Student Name' FROM students;
    SELECT first_name AS 'FIRST' , last_name AS 'Last' FROM students;   
    ```


4. Get all unique addresses of all students
        
    ```sql
    ***ANS 
    SELECT DISTINCT address  FROM students; 
    ```

5. Get all students with ID equal to 1
    
    ```sql 
    ***ANS
  SELECT * FROM students WHERE id=1; 
    ```


6. Get all students with IQ greater than 150 
    
    ```sql
    ***ANS
    SELECT iq FROM students WHERE iq>150;
    ```


7. Get all students with IQ less than 100
    
    ```sql
    ***ANS 
    SELECT iq FROM students WHERE iq<100;
    
    ```
8. Get all students with IQ greater than 100 and less than150

    ```sql
    ***ANS 
    SELECT iq FROM students iq=>  
    ```


9. Get all students with IQ greater than 100 or less than 150
    
    ```sql
    ***ANS 
    ```


10. Get all students with first name `Tantia`
    
    ```sql
    ***ANS
    SELECT * FROM students WHERE first_name ='Tantia';
    ```

11. Get all students with first name `Tantia` and last name `Tope`
    
    ```sql
    ***ANS 
    SELECT * FROM students WHERE first_name IN ('John','Mycroft','Anakin');
    ```

12. Get all students with first name `John` or first name `Mycroft` 
    ```sql
    ***ANS 
    SELECT * FROM students WHERE first_name ='John' OR first_name='Mycroft'; 
    ```

13. Get all students with name `John Watson` or `Mycroft Holmes` 
    ```sql
         
    
    ```
14. Get all students without the first name `John`
    
    ```sql
    ***ANS 
    SELECT * FROM students WHERE first_name NOT IN ('John');
    
    ```
15. Get all students without the first name `John` or first name `Mycroft`
    
    ```sql
    ***ANS 
    SELECT * FROM students WHERE first_name NOT IN ('John','Nycroft');
    
    ```
16. Get all students with first name starting with `T`
    
    ```sql
     ***ANS 
     SELECT * FROM students WHERE first_name LIKE 'T%';  
    ```

17. Get all students with last name ending with `walker`
    
    ```sql
    ***ANS 
    SELECT * FROM students WHERE last_name LIKE '%walker';
    
    ```
18. Get all students with first name containing `T`
    
    ```sql
     SELECT * FROM students WHERE first_name LIKE 'T%'; 
    
    ```
19. Get all students with last name in the format `___walker`
    ```sql
    
    ```
20. Get all students from Jhansi and London
    
    ```sql
    ***Ans 
    SELECT * FROM students WHERE address NOT IN ('Jhansi','London');
    
    ```
21. Get all students which do not have a batch id
    
    ```sql
    SELECT * FROM students WHERE batch_id IS NULL;

    
    ```
22. Get the first 5 students
    
    ```sql
    ***ANS 
    SELECT * FROM students WHERE id < 6;
    
    ```
23. Get the first 5 students sorted by IQ
    
    
    ```sql
    
    ```
24. Get the first 5 students sorted by IQ in descending order
    
    ```sql
    
    ```
25. Get the first 5 students sorted by IQ in descending order and then by first name
    
    ```sql
    
    ```
 
26. Selecting the date from particular date to date 

    SELECT * FROM batches WHERE start_date >= '2017-01-01' AND  start_date <= '2022-01-01';  

---

## Update Queries

1. Update a row

    ```sql
    
    ```
2. Update a row with a condition

    ```sql
    
    ```

3. Update multiple columns

    ```sql
    
    ```

## Delete Queries

1. Delete a row with a condition
 
     ```sql
     
     ```
 
2. Delete multiple rows
 
     ```sql
     
     ```

## Joining Queries

1. Get first name and last name of all students and their batch names
    
    ```sql
    
    ```
2. Get first name and last name of all students and their instructor names
    
    ```sql
    ```


    Got it! Here's a clear breakdown of all your SQL commands grouped by type:

---

















### 🛠️ **1. CREATE Commands**
> ❌ None of the `CREATE TABLE` commands were included in your script.

---

### ➕ **2. INSERT Commands**

#### 👨‍🎓 Students Table
```sql
INSERT INTO students (first_name, last_name, email, iq)
VALUES ("Moriarty", "Patel", "mo@sherlock.ed", 170);

INSERT INTO students (first_name, last_name , email) 
VALUES ('A', 'B','@gmail.com');
```

#### 🏫 Batches Table
```sql
INSERT INTO batches (name, start_date)
VALUES ("Crime Academy", "2022-10-01");
```

#### 👨‍🏫 Instructors Table
```sql
INSERT INTO instructors VALUES (7, 'A' , 'B' , 'email.com', 'phone');
INSERT INTO instructors VALUES (8, 'B','E','email','phone2');
INSERT INTO instructors (first_name , last_name , email) 
VALUES ('A','B','EMAIL');
INSERT INTO instructors VALUES(10,'K JITHENDHAR', 'REDDY' , 'EMAIL', 83929);
INSERT INTO instructors VALUES (12,'ROCK', 'JOHN', 'rockjohn@gmail.com', 1234567);
```

---

### 🔍 **3. SELECT Commands**

#### 🧾 Select All
```sql
SELECT * FROM instructors;
SELECT * FROM students;
SELECT * FROM batches;
```

#### 📌 With WHERE Conditions
```sql
SELECT * FROM instructors WHERE id > 11;
SELECT * FROM students WHERE id = 1;
SELECT * FROM students WHERE address = 'Meerut';
SELECT * FROM students WHERE address = 'jhansi';
SELECT * FROM students WHERE first_name = 'John';
SELECT * FROM students WHERE first_name = 'Mycroft';
SELECT * FROM students WHERE first_name = 'Anakin';
SELECT * FROM students WHERE first_name IN ('John','Mycroft','Anakin');
SELECT * FROM students WHERE first_name NOT IN ('John');
SELECT * FROM students WHERE address IN ('Jhansi' , 'Meerut', 'London');
SELECT * FROM students WHERE address NOT IN ('Jhansi','London');
SELECT * FROM batches WHERE instructor_id = 1;
SELECT * FROM batches WHERE start_date > '2022-01-01';
SELECT * FROM batches WHERE start_date >= '2017-01-01' AND start_date <= '2022-01-01';
SELECT * FROM batches WHERE start_date BETWEEN '2017-01-01' AND '2022-01-01';
SELECT * FROM students WHERE iq BETWEEN 100 AND 150;
SELECT * FROM students WHERE iq > 100 AND iq < 150;
SELECT iq FROM students WHERE iq > 150;
SELECT first_name, last_name, iq, address FROM students WHERE iq > 150 AND address = 'Meerut';
```

#### 🎯 Column Selection with Aliases
```sql
SELECT first_name AS 'FIRST', last_name AS 'Last' FROM students;
SELECT name AS 'full name', start_date FROM batches;
SELECT name AS 'FULL_NAME', start_date AS 'START' FROM batches;
SELECT first_name, last_name AS 'FULL NAME' FROM students;
```

#### 📞 Specific Columns
```sql
SELECT address FROM students;
SELECT email, phone FROM instructors;
```

#### 🔁 DISTINCT Usage
```sql
SELECT DISTINCT address FROM students;
SELECT DISTINCT id FROM students;
SELECT DISTINCT batch_id FROM students;
SELECT DISTINCT instructor_id FROM batches;
SELECT DISTINCT address FROM students WHERE batch_id > 2;
```

#### 🔗 CONCAT and Conditions
```sql
SELECT CONCAT(first_name, ' ' + last_name) AS Full_name FROM instructors 
WHERE last_name IN('Holmes','Odinson');

SELECT first_name, last_name FROM instructors 
WHERE last_name IN('Holmes', 'Odinson','Yoda');
```

---

### ❌ **4. UPDATE / DELETE Commands**
> None used in your script.

---

Let me know if you want this exported as a file or visualized as a flow!


Absolutely! The `LIKE` clause in SQL is used **to search for a specified pattern in a column**—and the `%` symbol is a **wildcard** that represents **zero or more characters**.

---

### 🧠 **Basic Syntax**
```sql
SELECT * FROM table_name WHERE column_name LIKE 'pattern';
```

---

### 🔣 **Wildcard: `%`**
- `%` matches **any number of characters**, including **zero characters**.

---

### ✅ **Examples with `LIKE` and `%`**

#### 1. Starts With
```sql
SELECT * FROM batches WHERE name LIKE 'jedi%';
```
✔️ This matches any name that **starts with "jedi"**, like:
- `jedi`
- `jedimaster`
- `jedicouncil`
- `jediskill`

#### 2. Ends With
```sql
SELECT * FROM batches WHERE name LIKE '%academy';
```
✔️ This matches any name that **ends with "academy"**, like:
- `jediacademy`
- `crimeacademy`
- `darkacademy`

#### 3. Contains
```sql
SELECT * FROM batches WHERE name LIKE '%crime%';
```
✔️ This matches any name that **contains "crime"** anywhere:
- `crimeacademy`
- `darkcrimeunit`
- `supercrimefighters`

---

### 🔍 More Patterns

| Pattern           | Meaning                                      |
|-------------------|----------------------------------------------|
| `'abc%'`          | Starts with "abc"                            |
| `'%abc'`          | Ends with "abc"                              |
| `'%abc%'`         | Contains "abc" anywhere                      |
| `'a%c'`           | Starts with "a" and ends with "c"            |
| `'____'`          | Exactly 4 characters (`_` = one character)   |
| `'a__%'`          | Starts with "a", then any 2 characters, then anything |

---

Let me know if you want to try some example data to test different `LIKE` patterns!
