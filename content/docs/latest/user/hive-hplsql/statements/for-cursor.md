---
title: "Apache Hive : HPL/SQL - FOR Statement (Cursor Loop)"
date: 2026-08-12
---

# Apache Hive : HPL/SQL - FOR Statement (Cursor Loop)

FOR statement opens a cursor, executes one or more statements repeatedly for each row and closes the cursor. 

Syntax:

```
FOR cur_name IN [(] select_stmt [)] LOOP
  statements
END LOOP;
```

**Notes:**

- You can refer to the cursor columns using *cur_name.col_name* syntax

**Example:**

```
FOR item IN (
    SELECT dname, loc as location
    FROM dept
    WHERE dname LIKE '%A%'
    AND deptno > 10
    ORDER BY location)
LOOP
  DBMS_OUTPUT.PUT_LINE('Name = ' || item.dname || ', Location = ' || item.location);
END LOOP;
```

**Compatibility:** Oracle, PostgreSQL and Netezza

<!-- **Version:** HPL/SQL 0.03 -->
