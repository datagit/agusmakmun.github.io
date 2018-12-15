---
layout: post
title:  "Data Types In PHP"
date:   2013-12-23 00:18:23 +0700
categories: [php]
tags: [data, type]
image: code_php_dummy.jpeg
---
PHP has a total of eight data types which we use to construct our variables:

* Integers − are whole numbers, without a decimal point, like 4195.
* Doubles − are floating-point numbers, like 3.14159 or 49.1.
* Booleans − have only two possible values either true or false.
* NULL − is a special type that only has one value: NULL.
* Strings − are sequences of characters, like 'PHP supports string operations.'
* Arrays − are named and indexed collections of other values.
* Objects − are instances of programmer-defined classes, which can package up both other kinds of values and functions that are specific to the class.
* Resources − are special variables that hold references to resources external to PHP (such as database connections).

Interpreting other types as Booleans
* Here are the rules for determine the "truth" of any value not already of the Boolean type
* If the value is a number, it is false if exactly equal to zero and true otherwise. 
* If the value is a string, it is false if the string is empty (has zero characters) or is the string "0", and is true otherwise. Values of type NULL are always false.
* If the value is an array, it is false if it contains no other values, and it is true otherwise. 
* For an object, containing a value means having a member variable that has been assigned a value.
* Valid resources are true (although some functions that return resources when they are successful will return FALSE when unsuccessful). Don't use double as Booleans.
```php
$true_num = 3 + 0.14159;
$true_str = "Tried and true"
$true_array[49] = "An array element";
$false_array = array();
$false_null = NULL;
$false_num = 999 - 999;
$false_str = "";
```
refer: [https://www.greycampus.com/codelabs/php/datatypes](https://www.greycampus.com/codelabs/php/datatypes)

Type Casting
We can cast following data type variable in PHP
* (int), (integer) - cast to integer
* (bool), (boolean) - cast to boolean
* (float), (double), (real) - cast to float
* (string) - cast to string
* (array) - cast to array
* (object) - cast to object
* (unset) - cast to NULL (PHP 5)

