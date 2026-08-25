---
title: "Apache Hive : HPL/SQL - Key Features"
date: 2026-08-12
---

# Apache Hive : HPL/SQL - Key Features

HPL/SQL key features:

- Flow of Control Statements (FOR, WHILE, IF, CASE, LOOP, LEAVE, RETURN)
- Functions, procedures, and packages
- Built-in functions (string manipulations, datetime functions, conversions)
- Exception handling and conditions
- Constants and variable, assignment (DECLARE count INT := 1)
- Processing results using a CURSOR
- On-the-fly SQL Conversion
- UDF to run HPL/SQL scripts from Hive queries
```
(SELECT hplsql('mycustomfunc(:1)', name) FROM users;)
```
