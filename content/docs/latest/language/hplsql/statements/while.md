---
title: "Apache Hive : HPL/SQL - WHILE Statement"
date: 2026-08-12
---

# Apache Hive : HPL/SQL - WHILE Statement

WHILE statement executes one or more statements while the condition is true. 

Syntax:

```
[<<label>> | label:]
WHILE boolean_expression LOOP | DO | BEGIN
  statements
END [LOOP | WHILE;]
```

**Examples:**

```
-- Oracle, PostgreSQL, Netezza
WHILE count > 0 LOOP
  count := count - 1;
END LOOP;
```

```
-- DB2, Teradata, MySQL
WHILE count > 0 DO
  SET count = count - 1;
END WHILE;
```

```
-- SQL Server
WHILE count > 0 BEGIN
  SET count = count - 1;
END
```

**Compatibility:** Oracle, Teradata, IBM DB2, Microsoft SQL Server, MySQL, PostgreSQL and Netezza.
