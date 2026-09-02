---
title: "Apache Hive : HPL/SQL - Get Started"
date: 2026-08-12
---

# Apache Hive : HPL/SQL - Get Started

Quick guide how to start using HPL/SQL.

You can enable and use HPL/SQL from any host or third-party tool that can make a JDBC connection to HiveServer. Beeline is a popular client for use with HPL/SQL because other third-party tools do not show you some of the error messages about syntax mistakes.

## Enabling HPL/SQL in the beeline connection string
After setting up a client to connect to HiveServer, you append ***mode=hplsql*** to the JDBC URL that connects the client to HiveServer.
```
beeline -u "jdbc:hive2://<HiveServer host>:10000/default;mode=hplsql"
```
When the client connects to HiveServer in this mode, HPL/SQL is enabled; otherwise, HPL/SQL is disabled.


At the Hive prompt, you can run HPL/SQL. You can use the forward slash(/) to switch Beeline to multiline mode for typing multiple rows and evaluating them at once.
```
0: jdbc:hive2://localhost> CREATE PROCEDURE greet(name STRING)
. . . . . . . . . . . . . . . . . . . . . . .> BEGIN
. . . . . . . . . . . . . . . . . . . . . . .>   PRINT 'Welcome to ' || name;
. . . . . . . . . . . . . . . . . . . . . . .> END;
. . . . . . . . . . . . . . . . . . . . . . .> /
No rows affected (0.084 seconds)
0: jdbc:hive2://localhost> greet('Apache Hive HPLSQL');/
INFO  : Welcome to Apache Hive HPLSQL
No rows affected (0.01 seconds)
0: jdbc:hive2://localhost>
```

You can use the existing beeline options like ***-e***, ***-f***. Below are the list of options that can be used in hplsql mode.

**Parameters:**

| Parameter | Description |
| --- | --- |
| -e 'query' | SQL statements to execute |
| -f file | Execute SQL statements from *file* |
| -main procname | Entry point (procedure or function name) |
| -d var=value | Variable definition |
| --define var=value | Variable definition |
| -hiveconf var=value | Variable definition |
| -hivevar var=value | Variable definition |


**Notes**:

- -e and -f cannot be specified together
- if -main option is not specified, HPL/SQL start executing all statements from the beginning of the script
- Currently -d, --define, -hivevar and -hiveconf are equivalent and allow you to define input variables.

**Example 1:**

Executing HPL/SQL statements from a script:

```
beeline -u "jdbc:hive2://<HiveServer host>:10000/default;mode=hplsql" -f script.hplsql 
```

**Example 2:**

Executing HPL/SQL statements from command line:

```
beeline -u "jdbc:hive2://<HiveServer host>:10000/default;mode=hplsql" -e "NVL(MAX_PARTITION_DATE(db.sales, local_dt, code='A'), CURRENT_DATE)" 
```

**Example 3:**

Using variables:

```
beeline -u "jdbc:hive2://<HiveServer host>:10000/default;mode=hplsql" -e "PRINT a || ', ' || b" -d a=Hello -d b=world 
```

Result:

```
Hello, world
```


