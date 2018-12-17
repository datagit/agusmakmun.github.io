---
layout: post
title:  "Mysql Data Types"
date:   2013-12-10 00:18:23 +0700
categories: [mysql]
tags: [mysql, mysql_data_types]
---

#### Here are most of the available column types for use with MySQL databases.

MySQL Datatypes

| Type | Size | Description | 
| ---------- | ----------  | ---------- |
| CHAR[Length] | Length bytes | A fixed-length field from 0 to 255 characters long. |
| VARCHAR(Length) | String length + 1 bytes | A fixed-length field from 0 to 255 characters long. |
| TINYTEXT | String length + 1 bytes | A string with a maximum length of 255 characters. |
| MEDIUMTEXT | String length + 3 bytes  | A string with a maximum length of 16,777,215 characters.  |
| LONGTEXT | String length + 4 bytes | A string with a maximum length of 4,294,967,295 characters.  |
| TINYINT[Length] | 1 byte  | Range of -128 to 127 or 0 to 255 unsigned.  |
| SMALLINT[Length] | 2 bytes  | Range of -32,768 to 32,767 or 0 to 65535 unsigned.  |
| MEDIUMINT[Length] | 3 bytes  | Range of -8,388,608 to 8,388,607 or 0 to 16,777,215 unsigned.  |
| INT[Length] | 4 bytes  | Range of -2,147,483,648 to 2,147,483,647 or 0 to 4,294,967,295 unsigned.  |
| BIGINT[Length] | 8 bytes  | Range of -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 or 0 to 18,446,744,073,709,551,615 unsigned.  |
| FLOAT | 4 bytes  | A small number with a floating decimal point.  |
| DOUBLE[Length, Decimals] | 8 bytes  | A large number with a floating decimal point.  |
| DECIMAL[Length, Decimals] | Length + 1 or Length + 2 bytes  | A DOUBLE stored as a string, allowing for a fixed decimal point.  |
| DATE | 3 bytes  | In the format of YYYY-MM-DD.  |
| DATETIME | 8 bytes  | In the format of YYYY-MM-DD HH:MM:SS.  |
| TIMESTAMP | 4 bytes  | In the format of YYYYMMDDHHMMSS; acceptable range ends inthe year 2037.  |
| TIME | 3 bytes  | In the format of HH:MM:SS  |
| ENUM | 1 or 2 bytes  | Short for enumeration, which means that each column can haveone of several possible values.  |
| SET | 1, 2, 3, 4, or 8 bytes  | Like ENUM except that each column can have more than one ofseveral possible values.  |


**Refference:** [http://www.peachpit.com/articles/article.aspx?p=30885&seqNum=7](http://www.peachpit.com/articles/article.aspx?p=30885&seqNum=7)

hope it usefull.