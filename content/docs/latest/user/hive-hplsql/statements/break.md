---
title: "Apache Hive : HPL/SQL - BREAK Statement"
date: 2026-08-12
---

# Apache Hive : HPL/SQL - BREAK Statement

BREAK statement exits the innermost loop. 

Syntax:

```
BREAK;
```

**Example:**

```
DECLARE count INT DEFAULT 3;
WHILE 1=1 BEGIN
  SET count = count - 1;
  IF count = 0
    BREAK;
END
```

**Compatibility:** Microsoft SQL Server.
