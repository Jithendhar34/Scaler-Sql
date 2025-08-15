Got it ✅
Here’s a **full README.md** with **definitions, examples, and a relationship diagram** for **all SQL keys**, including the **Super Key example**.

---

````markdown
# SQL Keys – Definitions, Examples, and Diagram

## 1. Primary Key
**Definition:**  
A column (or combination of columns) that uniquely identifies each row in a table.

**Rules:**
- Must be **unique**
- Cannot be **NULL**

**Example:**
```sql
emp_id INT PRIMARY KEY
````

---

## 2. Foreign Key

**Definition:**
A column in one table that refers to the **Primary Key** in another table to maintain **referential integrity**.

**Example:**

```sql
FOREIGN KEY (dept_id) REFERENCES Departments(dept_id)
```

---

## 3. Unique Key

**Definition:**
Ensures all values in a column are **unique** (like Primary Key) but allows **one NULL** (depending on DBMS).

**Example:**

```sql
email VARCHAR(100) UNIQUE
```

---

## 4. Candidate Key

**Definition:**
All columns that can uniquely identify rows in a table.
The **Primary Key** is chosen from the candidate keys.

**Example:**
In a `Students` table:

* `student_id` → Unique
* `email` → Unique
  Both are **candidate keys**.

---

## 5. Alternate Key

**Definition:**
Candidate keys that are **not** chosen as the Primary Key.

**Example:**
If `student_id` is Primary Key, then `email` is an Alternate Key.

---

## 6. Composite Key

**Definition:**
A key formed by combining two or more columns to uniquely identify a row.

**Example:**

```sql
PRIMARY KEY (order_id, product_id)
```

---

## 7. Super Key

**Definition:**
Any set of columns that can uniquely identify a row (includes candidate keys + extra columns).

**Example:**

```sql
CREATE TABLE Students (
    student_id INT,
    email VARCHAR(100),
    phone VARCHAR(15),
    PRIMARY KEY (student_id)
);

-- Examples of Super Keys:
-- {student_id}
-- {student_id, email}
-- {student_id, phone}
-- {student_id, email, phone}
```

All above combinations **uniquely identify** a student, so they are **Super Keys**.

---

## 8. Surrogate Key

**Definition:**
An artificially generated key (often auto-increment ID) used instead of a natural key.

**Example:**

```sql
id INT AUTO_INCREMENT PRIMARY KEY
```

---

## 🔹 Quick Comparison Table

| Key Type      | Unique Values | Allows NULL | Purpose                                 |
| ------------- | ------------- | ----------- | --------------------------------------- |
| Primary Key   | ✅ Yes         | ❌ No        | Unique row identification               |
| Unique Key    | ✅ Yes         | ✅ Yes (1)   | Uniqueness without being primary        |
| Foreign Key   | ❌ No          | ✅ Yes       | Maintain relationship between tables    |
| Candidate Key | ✅ Yes         | ❌/✅         | All possible unique identifiers         |
| Alternate Key | ✅ Yes         | ❌/✅         | Candidate keys not chosen as PK         |
| Composite Key | ✅ Yes         | ❌ No        | Unique ID using multiple columns        |
| Super Key     | ✅ Yes         | ❌/✅         | Any column set that uniquely identifies |
| Surrogate Key | ✅ Yes         | ❌ No        | System-generated unique ID              |

---

## 📌 Relationship Diagram

```text
            ┌─────────────┐
            │ Super Key   │
            └──────┬──────┘
                   │
           ┌───────┴────────┐
           │ Candidate Key  │
           └──────┬─────────┘
        ┌─────────┴───────────┐
        │ Primary Key         │
        │ Alternate Key       │
        └─────────────────────┘
```

* **Super Key** → All possible unique combinations
* **Candidate Keys** → Minimal unique combinations
* **Primary Key** → Chosen candidate key
* **Alternate Key** → Other candidate keys not chosen as primary

---

## ✅ Summary

* **Primary Key** → Main unique identifier (no NULLs)
* **Foreign Key** → Links to another table's Primary Key
* **Unique Key** → Enforces uniqueness (NULL allowed once)
* **Candidate Key** → All possible unique identifiers
* **Alternate Key** → Candidate key not used as Primary Key
* **Composite Key** → Uses multiple columns for uniqueness
* **Super Key** → Any unique column set (includes extra columns)
* **Surrogate Key** → Artificially generated key

```

---

If you want, I can also **make this diagram in an image format** with colors and arrows so it looks professional for your README on GitHub.  
Do you want me to prepare that visual diagram?
```
