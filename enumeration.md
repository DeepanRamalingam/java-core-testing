---
layout: main
title: Enumeration
previousLink: ./exceptional-handling
previousTitle: Exceptional Handling
nextLink: ./multithreaded-programming-in-java
nextTitle: Multithreaded Programming in Java
duration: 
---

# Enumeration  

### Objectives

- What is Enum?
- How to define Enum type?
- Enum Example
- Enum with parameter
- Traversing Enum
- Enum Vs Class with static final(constants)
- Benefits of Enums in Java


### What is Enum?

- A Java Enum is a special Java type used to define collections of
    constants.
- More precisely, a Java enum type is a special kind of Java class.
- An enum can contain constants, methods etc. Java enums were
    added in Java 5.


### How to define enum type?

- In the Java programming language, you define an enum type by using the
    enum keyword.
- For example, you would specify a days-of-the-week enumtype as:

public enum Day {

```
SUNDAY, MONDAY, TUESDAY, WEDNESDAY,
THURSDAY, FRIDAY, SATURDAY
```
}


### Enum Example


### Enum Example - Test


### Enum with parameter


### Enum with parameter - Test


### Traversing Enum

```
Output:
```

### Enum Vs Class with static final(constants)


### What if we used static final in class?

- No Type-Safety: Can assign any valid int value.
- No Meaningful Printing: printing value of any of these constant will
    print its numeric value instead of meaningful name.


### Benefits of Enums in Java

- Enum is type-safe you can not assign anything else other than predefined Enum
    constants to an Enum variable.
- It is compiler error to assign something else unlike the public static final variables
    used in Enumintpattern and Enum String pattern.
- Enum has its own name-space.
- Best feature of Enum is you can use Enumin Java inside Switch statementlike int
    or char primitive data type.
- Adding new constants on Enum in Java is easy and you can add new constants
    without breaking existing code.


### Benefits of Enums in Java

- Java compiler automatically generates static values() method for
    every enum in java.
- Values() method returns array of Enum constants in the same order
    they have listed in Enum and you can use values() to iterate over
    values of Enum in Java as shown in below example:


# QUIZ


- What is enum in java?


- A Java Enum is a special Java type used to define collections of
    constants.


- How to define enum type?


- Using enum keyword.

public enum EnumName{

```
//set of constants
//methods
```
}

- Example

public enum Day {

```
SUNDAY, MONDAY, TUESDAY, WEDNESDAY,
THURSDAY, FRIDAY, SATURDAY
```
}


# MR


### Excercises

- Create an enum with different constants called add,sub,mul,div and
    define a method called calculate. Test all the operations.
- Create an enum with month with maximumum no.of days in each
    month. Display all the months with maximumum no.of days in each
    month.


