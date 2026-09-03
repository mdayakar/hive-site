---
title: "Apache Hive : HPL/SQL - RETURN Statement"
date: 2026-08-12
---

# Apache Hive : HPL/SQL - RETURN Statement

RETURN statement is used to return from a routine. 

**Syntax:**

```
RETURN [expr];
```

**Parameters:**

| **Parameter** | **Type** | **Value** | **Description** |
| --- | --- | --- | --- |
| expr | INT | Variable or expression | Return value |

**Notes**:

- If the return value is not specified, 0 is returned

**Examples:**

```
RETURN;
```

Return the result of an expression:

```
RETURN NVL(v1, 1);
```

**Compatibility:** Oracle, IBM DB2, SQL Server, Teradata, PostgreSQL, MySQL, Netezza.

<!-- **Version:** HPL/SQL 0.01 -->
