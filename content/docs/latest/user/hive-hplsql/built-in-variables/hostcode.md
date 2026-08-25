---
title: "Apache Hive : HPL/SQL - HOSTCODE"
date: 2026-08-12
---

# Apache Hive : HPL/SQL - HOSTCODE

HOSTCODE built-in variable contains the return code of the last OS command. 

```
SET hplsql.onerror = SETERROR;

HOST 'echo hello, world';
IF HOSTCODE <> 0 THEN
  PRINT 'Error';
END IF;
```

**Notes**:

- Typically HOSTCODE is 0 when the process terminated successfully, and 1 if it terminated with an error.
- By default [hplsql.onerror]({{< ref "configuration#hplsqlonerror" >}}) is set to EXCEPTION, so if the OS command cannot be executed (the process does not exist, no permissions i.e.) the exception is raised and you are not be able to check HOSTCODE in IF statement.

For more information, see [Error Handling]({{< ref "error-handling" >}}).

**Compatibility:** HPL/SQL Extension.

**See also:**
- [SQLCODE]({{< ref "sqlcode" >}})
