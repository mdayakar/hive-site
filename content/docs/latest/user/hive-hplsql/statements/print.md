---
title: "Apache Hive : HPL/SQL - PRINT Statement"
date: 2026-08-12
---

# Apache Hive : HPL/SQL - PRINT Statement

PRINT statement prints a line and can be helpful to debug programs. The statement appends a line terminator. 

**Syntax:**

```
PRINT exp
or
PRINT(exp)
```

**Parameters:**

| **Parameter** | **Type** | **Description** |
| --- | --- | --- |
| exp | VARCHAR | Text string or expression | 

**Return Value:**

No.

**Examples:**

```
PRINT 'Hello, world!';
PRINT 'Hello, ' || 'world!';
PRINT('Hello, world!');
```

**Compatibility**: Microsoft SQL Server
