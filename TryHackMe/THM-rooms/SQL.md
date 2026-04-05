# SQL Basics – Quick Reference (MySQL)

## 📌 General Notes

- SQL = Structured Query Language
- Used to interact with databases
- Syntax is NOT case-sensitive
- Every statement ends with `;`

---

## 🔍 SELECT – Retrieve Data

### Get all columns

SELECT \* FROM users;

### Get specific columns

SELECT username, password FROM users;

### Limit results

SELECT _ FROM users LIMIT 1; -- first row  
SELECT _ FROM users LIMIT 1,1; -- skip 1, return 1  
SELECT \* FROM users LIMIT 2,1; -- skip 2, return 1

---

## 🎯 WHERE – Filter Data

### Exact match

SELECT \* FROM users WHERE username = 'admin';

### Not equal

SELECT \* FROM users WHERE username != 'admin';

### Multiple conditions

SELECT _ FROM users WHERE username = 'admin' OR username = 'jon';  
SELECT _ FROM users WHERE username = 'admin' AND password = 'p4ssword';

---

## 🔎 LIKE – Pattern Matching

- 'a%' → starts with a
- '%n' → ends with n
- '%mi%' → contains mi

### Examples

SELECT _ FROM users WHERE username LIKE 'a%';  
SELECT _ FROM users WHERE username LIKE '%n';  
SELECT \* FROM users WHERE username LIKE '%mi%';

---

## 🔗 UNION – Combine Results

Rules:

- Same number of columns
- Compatible data types
- Same column order

### Example

SELECT name, address, city, postcode FROM customers  
UNION  
SELECT company, address, city, postcode FROM suppliers;

---

## ➕ INSERT – Add Data

INSERT INTO users (username, password)  
VALUES ('bob', 'password123');

---

## ✏️ UPDATE – Modify Data

UPDATE users  
SET username = 'root', password = 'pass123'  
WHERE username = 'admin';

⚠️ Without WHERE → all rows are modified

---

## ❌ DELETE – Remove Data

### Delete specific row

DELETE FROM users WHERE username = 'martin';

### Delete all rows

DELETE FROM users;

⚠️ Without WHERE → deletes everything

---

## 🧠 Key Takeaways

- SELECT → read data
- INSERT → add data
- UPDATE → modify data
- DELETE → remove data
- WHERE → filter results
- LIKE → pattern matching
- LIMIT → control result size
- UNION → combine results

---

## 🚀 Tip

Always verify UPDATE and DELETE queries before executing them.  
Missing WHERE can wipe an entire table.
