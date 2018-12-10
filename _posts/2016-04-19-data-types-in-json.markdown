---
layout: post
title:  "Data Types In Json"
date:   2016-04-19 19:31:43 +0700
categories: [json]
---
Because JSON is designed to be lightweight, it supports only four primitive data types, as shown in the following table.
#### Table 1. JSON primitive data types
Data type | Description | Examples
------------ | ------------- | -------------
string | A string of Unicode characters enclosed in double quotes. A backslash ( \ ) serves as the escape character. | "jump rope"
number | An unquoted numeric value, which can include an exponent | 1754.350.9582e-42
boolean | An unquoted lowercase literal string of true or false | true
null | An unquoted lowercase literal string of null | null

JSON also supports two complex data types, as shown in the following table:

Data type | Description | Examples
------------ | ------------- | -------------
Object | A comma-delimited list of named values, either simple or complex, enclosed in braces | { "myString" : "jump rope",   "myNum" : 17, "myBool" : false }
Array | A comma-delimited list of unnamed values, either simple or complex, enclosed in brackets | [ "jump rope", 17, false ]

refer: [https://documentation.progress.com/output/ua/OpenEdge_latest/index.html#page/dvjsn%2Fjson-data-types.html%23](https://documentation.progress.com/output/ua/OpenEdge_latest/index.html#page/dvjsn%2Fjson-data-types.html%23)