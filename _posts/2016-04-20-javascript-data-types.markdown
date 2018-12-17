---
layout: post
title:  "Javascript Data Types"
date:   2016-04-20 19:31:43 +0700
categories: [javascript]
tags: [javascript, json_data_types]
---
#### A number
```javascript
var n = 123;
n = 12.345;
```

The number type serves both for integer and floating point numbers.

There are many operations for numbers, e.g. multiplication *, division /, addition +, subtraction - and so on.

Besides regular numbers, there are so-called “special numeric values” which also belong to that type: Infinity, -Infinity and NaN.

Infinity represents the mathematical Infinity ∞. It is a special value that’s greater than any number.

We can get it as a result of division by zero:
```javascript
alert( 1 / 0 ); // Infinity
```
Or just mention it in the code directly:
```javascript
alert( Infinity ); // Infinity
```
NaN represents a computational error. It is a result of an incorrect or an undefined mathematical operation, for instance:
```javascript
alert( "not a number" / 2 ); // NaN, such division is erroneous
```
NaN is sticky. Any further operation on NaN would give NaN:
```javascript
alert( "not a number" / 2 + 5 ); // NaN
```
So, if there’s NaN somewhere in a mathematical expression, it propagates to the whole result.

#### Mathematical operations are safe
Doing maths is safe in JavaScript. We can do anything: divide by zero, treat non-numeric strings as numbers, etc.

The script will never stop with a fatal error (“die”). At worst we’ll get NaN as the result.

#### A string in JavaScript must be quoted.
```javascript 1.8
let str = "Hello";
let str2 = 'Single quotes are ok too';
let phrase = `can embed ${str}`;
```

In JavaScript, there are 3 types of quotes.

- Double quotes: "Hello".
- Single quotes: 'Hello'.
- Backticks: `Hello`.

```javascript 1.8
let name = "John";

// embed a variable
alert( `Hello, ${name}!` ); // Hello, John!

// embed an expression
alert( `the result is ${1 + 2}` ); // the result is 3
```
#### A boolean (logical type)
The boolean type has only two values: true and false.

This type is commonly used to store yes/no values: true means “yes, correct”, and false means “no, incorrect”.

For instance:
```javascript 1.8
let nameFieldChecked = true; // yes, name field is checked
let ageFieldChecked = false; // no, age field is not checked
```

#### The “null” value
The special null value does not belong to any type of those described above.

It forms a separate type of its own, which contains only the null value:
```javascript 1.8
let age = null;
```

##### The “undefined” value
The special value undefined stands apart. It makes a type of its own, just like null.

The meaning of undefined is “value is not assigned”.

If a variable is declared, but not assigned, then its value is exactly undefined:
```javascript 1.8
let x;
alert(x); // shows "undefined"

let x = 123;
x = undefined;
alert(x); // "undefined"
```

#### The typeof operator
The typeof operator returns the type of the argument. It’s useful when we want to process values of different types differently, or just want to make a quick check.

It supports two forms of syntax:

- As an operator: typeof x.
- Function style: typeof(x).
```javascript 1.8
typeof undefined // "undefined"

typeof 0 // "number"

typeof true // "boolean"

typeof "foo" // "string"

typeof Symbol("id") // "symbol"

typeof Math // "object"  (1)

typeof null // "object"  (2)

typeof alert // "function"  (3)
```

#### Summary
There are 7 basic types in JavaScript.

- number for numbers of any kind: integer or floating-point.
- string for strings. A string may have one or more characters, there’s no separate single-character type.
- boolean for true/false.
- null for unknown values – a standalone type that has a single value null.
- undefined for unassigned values – a standalone type that has a single value undefined.
- object for more complex data structures.
- symbol for unique identifiers.
- The typeof operator allows us to see which type is stored in the variable.

Two forms: typeof x or typeof(x).

Returns a string with the name of the type, like "string".

For null returns "object" – that’s an error in the language, it’s not an object in fact.


**Refference:** 
[https://javascript.info/types](https://javascript.info/types)

hope it usefull.
