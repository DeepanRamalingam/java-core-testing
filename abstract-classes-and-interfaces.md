---
layout: main
title: Abstract Classes and Interfaces
previousLink: ./object-oriented-programming-concepts
previousTitle: Object Oriented Programming Concepts
nextLink: ./working-with-arrays
nextTitle: Working with Arrays
duration: 
---

# Abstract Classes and Interfaces  

### AGENDA

- Interfaces and Abstract Class
    - What is Interface
    - What are the uses of interface
    - How to implement interface
    - What is abstract class
    - What are the differences between interface and abstract class.
- Associations between classes


### What is interface

- An **interface in java** is a blueprint of a class.
- It has static constants and abstract methods.
- The **interface in java** is a mechanism to achieve abstraction.
- There can be only abstract methods in the **java interface** not method
    body.
- It specifies what to do, not how to do(implement)
- For same interface, we may have multiple implementation.


Will discuss later..


### Interface - syntax

```
Implementation
```

### Example


### Multiple implementation


### What is @Override here?

- It is an Annotation (will discuss later)
- It is optional, but better to use it.
- If programmer makes any mistake such as wrong method name, wrong
    parameter types while overriding, you would get a compile time error.
- As by using this annotation you instruct compiler that you are overriding this
    method.
- If you don’t use the annotation then the sub class method would behave as
    a new method (not the overriding method) in sub class.
- If you change the signature of overridden method then all the sub classes
    that overrides the particular method would throw a compilation error, which
    would eventually help you to change the signature in the sub classes.


### Abstraction

- What is Abstraction
- Why Abstraction
- How to achieve abstraction in java
- Difference between abstraction and encapsulation
- Interfaces and Abstract Class
    - What is Interface
    - What is abstract class
    - What are the differences between interface and abstract class.


### What is abstract class?

- An **abstract class** can have **abstract** method without body and it can
    have methods with implementation also.
- **abstract** keyword is used to create a **abstract class** and method.
- **Abstract class in java** can't be instantiated
- An abstract method is a method that is declared, but contains no
    implementation.
- An abstract class may have static fields and static methods.


### What is abstract class?

- An abstract class can be used as a type of template for other classes,
    and most commonly used for inheritance.
- Can provide default behaviour for common functionality.
- This default behaviour can be used by all the children/sub classes
    without redefining it.


### Example – abstract class

```
Will discuss “extends” i.e., inheritance later
```

### Interface Vs Abstract Class


# Associations between

# the classes


### How access other class properties

- If you want to access properties of one class A in class B
    - Should I use inheritance? Like class B extends A
    - OR
    - Create instance of class A in Class B?
- Which is better?


### Which is better?

- It is based on what type of relation is there between the classes.


### What are the types relationship?

- Generalization
- Aggregation
- Composition


### Generalization

- If the relationship is “kind of” / “type of” / “is a”
- Achieved by inheritance
- Ex:
    - ContractEmployeeis kind of Employee
    - SavingAccountis kind of Account
    - Truck is kind of Vehicle


### Aggregation

- If the relationship is “part of” / “ has a”
- Relationship should be loosely coupled
- Achieved by creating objects
- Ex:
    - Department has Employees
    - Employee has Address


### Composition

- If the relationship is “part of” / “has a”
- Relationship should be tightly coupled
- Achieved by creating objects
- Ex:
    - Book has pages


# QUIZ


##### • MR


### Understanding Abstract class and Interface

- Create Account interface
- Declare methods for openAccout, closeAccountand getBalancewith proper method signature
- Create an abstract class called AbstractAccount
    - • Implements Keep other two methods as abstract methodsgetBalancemethod()
- Create Two classes SavingAccountand DepositAccount
- Extend AbstractAccountin both SavingAccountand DepositAccount
- Implement openAccountand closeAccountmethods
    - Just write print statements.
- Create AccountTestclass
- In main method
    - • Create Create SavingAccountDepositAccountinstance and call the methodsinstance and call the methods


