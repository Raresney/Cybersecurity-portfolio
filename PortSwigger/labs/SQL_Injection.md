# SQL Injection

SQL injection is a classic vulnerability responsible for many high-profile data breaches. It enables an attacker to interfere with the queries the application issues to its database, potentially returning sensitive data from arbitrary tables.

---

## Labs Completed (7/7)

| # | Lab | Level |
| --- | --- | --- |
| 1 | SQL injection vulnerability in WHERE clause allowing retrieval of hidden data | Apprentice |
| 2 | SQL injection vulnerability allowing login bypass | Apprentice |
| 3 | SQL injection UNION attack, determining the number of columns | Practitioner |
| 4 | SQL injection UNION attack, finding a column containing text | Practitioner |
| 5 | SQL injection UNION attack, retrieving data from other tables | Practitioner |
| 6 | SQL injection UNION attack, retrieving multiple values in a single column | Practitioner |
| 7 | Examining the database in SQL injection attacks | Practitioner |

---

## Key Concepts

### What is SQL Injection?
- Inserting malicious SQL into application queries via user-controlled input
- Can read, modify, or delete data and potentially compromise the server

### Detecting SQLi
- Submitting `'`, `"`, `--`, `;` and observing errors or behavioral changes
- Boolean-based: `' OR 1=1--` vs `' OR 1=2--`
- Time-based: `'; WAITFOR DELAY '0:0:10'--`

### Retrieving Hidden Data
- Manipulating WHERE clauses to bypass filters (e.g., `' OR 1=1--`)
- Exposing unreleased or hidden records

### Subverting Application Logic
- Login bypass: `administrator'--` to comment out password check

### UNION Attacks
- Determining column count: `ORDER BY n` or `UNION SELECT NULL,NULL,...`
- Finding text-compatible columns for data extraction
- Retrieving data from other tables (e.g., `users`)
- Concatenating multiple values in a single column (`username || ':' || password`)
