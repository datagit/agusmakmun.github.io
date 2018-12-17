---
layout: post
title:  "Mysql row count"
date:   2016-04-19 19:39:02 +0700
categories: [mysql]
---
#### Getting MySQL row count of all tables in a database with one query
Getting MySQL row count of two or more tables
To get the row count of multiple tables, you use the UNION operator to combine result sets returned by each individual SELECT statement.

For example, to get the row count of customers and orders tables in a single query, you use the following statement.
```sql
SELECT 
    'customers' tablename, 
     COUNT(*) rows
FROM
    customers 
UNION 
SELECT 
    'orders' tablename, 
     COUNT(*) rows
FROM
    orders;
```
result:
```
+-----------+------+
| tablename | rows |
+-----------+------+
| customers |  122 |
| orders    |  326 |
+-----------+------+
2 rows in set (0.01 sec)
```

A quick way to get the row count of all tables in a database is querying data from the information_schema database directly:

```sql
SELECT 
    table_name, 
    table_rows
FROM
    information_schema.tables
WHERE
    table_schema = 'classicmodels'
ORDER BY table_name;
```

![see](http://www.mysqltutorial.org/wp-content/uploads/2017/07/MySQL-Row-Count.png)

**Refference:** 
[http://www.mysqltutorial.org/mysql-row-count/](http://www.mysqltutorial.org/mysql-row-count/)

hope it usefull.
