---
title: "Apache Hive : HPL/SQL - TRIM Function"
date: 2026-08-12
---

# Apache Hive : HPL/SQL - TRIM Function

TRIM function removes leading and trailing characters from a string.

**Syntax**:

```
TRIM(string_expression); 
```

**Return Type:**

STRING

**Example 1:**

```
'#' || TRIM(' Hello ') || '#'; 
--
#Hello#
```

**Compatibility**: Oracle, IBM DB2, Teradata, Microsoft SQL Server, PostgreSQL, MySQL and Netezza

<!-- **Version**: HPL/SQL 0.03 -->
