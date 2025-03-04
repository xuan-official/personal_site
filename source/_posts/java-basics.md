---
title: Java Language Basics
date: 2025-03-03 10:31:19
categories:
- Java
tags: 
---

# 1 Creating variables and naming them

## 1.1 Variables

```java
int cadence = 0;
int speed = 0;
int gear = 1;
```

The Java programming language defines the following kinds of variables:

* Instance Variables (Non-Static Fields)
* Class Variables (Static Fields)
* Local Variables
* Parameters

## 1.2 Naming Variables

# 2 Creating Primitive Type Variables

## 2.1 Primitive Types

&emsp;&emsp;The Java programming language is *statically-typed*, which means that all variables must first be declared before they can be used.

This involves stating the variable's type and name, as shown below:

```java
int gear = 1;
```

Doing so tells the program that a field named `gear` exists, holds numerical data, and has an initial value of `1`. 

&emsp;&emsp;In addition to `int`, the Java programming language supports seven other primitive data types. A primitive type is predefined by the language and is named by a reserved keyword. 

The eight primitive data types supported by the Java programming language are:

<img src="/images/java-8-primitive-datatypes.png">

&emsp;&emsp;In addition to the eight primitive data types listed above, the Java programming language also provides special support for character strings via the `java.lang.String` class.

Enclosing the character string within double quotes will automatically create a new `String` object

```java
String s = "this is a string";
```

> But in any case, the String class is not technically a primitive data type.

## 2.2 Initializing a Variable with a Default Value

&emsp;&emsp;It is not always necessary to assign a value when a field is declared. **Fields** that are declared but not initialized will be set to a reasonable default by the compiler. 

Generally speaking, this default will be **zero** or **null**, depending on the data type. However, relying on such default values, however, *is generally considered bad programming style*.

The following table summarizes the default values for the above data types.

|        Data Type         | Default Value (for fields) |
| :----------------------: | :------------------------: |
|          `byte`          |            `0`             |
|         `short`          |            `0`             |
|          `int`           |            `0`             |
|          `long`          |            `0L`            |
|         `float`          |           `0.0f`           |
|         `double`         |           `0.0d`           |
|          `char`          |          `\u0000`          |
| `String` (or any object) |           `null`           |
|        `boolean`         |          `false`           |

Local variables are slightly different; the compiler never assigns a default value to an uninitialized local variable.

If a local variable is not initialized where it is declared, we need to make sure to assign it a value before we attempt to use it. Accessing an uninitialized local variable will result in a compile-time error.

## 2.3 Creating Values with Literals

