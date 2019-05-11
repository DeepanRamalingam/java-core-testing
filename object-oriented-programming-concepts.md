---
layout: main
title: Object Oriented Programming Concepts
previousLink: ./java-language-fundamentals
previousTitle: Java Language Fundamentals
nextLink: ./abstract-classes-and-interfaces
nextTitle: Abstract Classes and Interfaces
duration: 
---

# Object Oriented Programming Concepts  

### Objectives

- What is OOP
- Class
- Object
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism


#### What is OOP

- Object-oriented programming is a programming paradigm based on
    the concept of "objects“.
- Objects contain data, in the form of fields; and code, in the form of
    methods


#### Class

A class is
Collection of data members + member functions
A User defined data type
A Template/Blueprint/Prototype used to create objects


#### Class


### What is access specifier?

- **Java Access Specifiers** (also known as Visibility **Specifiers** )
    regulate **access** to classes, fields and methods in **Java**.
- These **Specifiers** determine whether a field or method in a class, can
    be used or invoked by another method in another class or sub-class.
- **Access Specifiers** can be used to restrict **access**.


### Class Definition - syntax


### Example – Class - Student


### What is method?

- A **Java method** is a collection of statements that are grouped together
    to perform an operation


### Objectives

- What is OOP
- Class
- Object
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism


### Object

- An **object** is an instance of a class.
- A class can be defined as a template/blueprint that describes the
    behaviour/state that the **object** of its type support.


### Class and Object


### How to create object?


### What is constructor?


### Objectives

- What is OOP
- Class
- Object
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism


### Encapsulation

- What is Encapsulation?
- Why Encapsulation?
- How Is Encapsulation Done in Java?


### What Encapsulation?

- **Encapsulation** in **Java** is a mechanism of wrapping the data and
    methods together as a single unit
- Encapsulation is a technique for protecting data from misuse by the
    outside world, which is referred as ‘ **_information hiding_** ’ or ‘ **_data_**
    **_hiding_** ’.
       - By using private access specifier for properties


#### Why Encapsulation?

- **Flexibility** :
    - It’s more flexible and easy to change the encapsulated code with new
       requirements.
    - For example, if the requirement for setting the age of a person changes, we can
       easily update the logic in the setter methodsetAge().
- **Reusability** :
    - Encapsulated code can be reused throughout the application or across multiple
       applications.
    - For example, the Person class can be reused whenever such type of object is
       required.
- **Maintainability** :
    - Application ode is encapsulated in separate units (classes, interfaces, methods,
       setters, getters, etc) so it’s easy to change or update a part of the application
       without affecting other parts, which reduces the time of maintenance.


#### How Is Encapsulation Done in Java?

- Encapsulation is implemented in Java using interfaces, classes, access
    modifiers, setters and getters.
- A class or an interface encapsulates essential features of an object.
- Access modifiers (private, public, protected) restrict access to data at
    different levels.
- Setters and getters prevent data from misuse or unwanted changes
    from other objects.


### Encapsulation - Example


### Objectives

- What is OOP
- Class
- Object
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism
- Object Associations


### Abstraction

- What is Abstraction
- Why Abstraction
- How to achieve abstraction in java
- Difference between abstraction and encapsulation


#### What is Abstraction

- **Abstraction** is a process of hiding the implementation details from
    the outside.
- Оnly the functionality will be provided to the user.


#### Why Abstraction

- We should not expose implementation details out side of the world.
- We may have multiple implementation for same type of operations.


#### How to achieve abstraction in java

- In **Java** , **abstraction** is achieved using **abstract** classes and interfaces.
- Will discuss in next session.


#### Difference between abstraction and encapsulation


### Objectives

- What is OOP
- Class
- Object
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism
- Object Associations


#### Inheritance

- What is Inheritance
- When should I use Inheritance?
- How to achieve Inheritance?


### What is Inheritance

- **Inheritance** is a mechanism wherein a new class is derived from an
    existing class.
- In **Java** , classes may **inherit** or acquire the properties and methods of
    other classes.
- A class derived from another class is called a subclass, whereas the
    class from which a subclass is derived is called a superclass.


### When should I use inheritance

- If the relationship between the Classes are “kind of” or “type of”
    relationship.
- Example
    - Car is a type of Vechicle
    - ContractEmployeeis a type of Employee
    - SavingAccount is a type of Account


### How to achieve Inheritance

- Using extends key word


### Inheritance - Example


### Multi Level Inheritance


### Objectives

- What is OOP
- Class
- Object
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism
- Object Associations


### Polymorphism

- What is polymorphism
- Types of polymorphism
- Constructor overloading


### What is polymorphism?

- The word "poly" means many and "morphs" means forms.
- So polymorphism means many forms.


### Types of Polymorphism

- Static Polymorphism (Compile time Polymorphism )
- Dynamic Polymorphism (Run time Polymorphism )


### Static Polymorphism

- Static polymorphism is achieved through method overloading.
- Method overloading means there are several methods present in a
    class having the same name but different types/order/number of
    parameters.


### Example – Static Polymorphism


### Run time polymorphism

- **Runtime polymorphism** or **Dynamic Method Dispatch** is a process in
    which a call to an overridden method is resolved at runtime rather
    than compile-time.
- In this process, an overridden method is called through the reference
    variable of a superclass. The determination of the method to be
    called is based on the object being referred to by the reference
    variable.


### Run Time Polymorphism - example

```
call
```
```
call
```

#### Constructor overloading

- Each class has default constructor (with no arguments)
- Constructor will be called when you create object with “new” operator.
- You can create your own constructor


### Why constructor overloading required?

- When you want to set parameters, you can use setter methods.
- But, setter methods should be used for
    - optional parameters
    - Parameters which are changed in future.
- Mandatory parameter should be set by constructor.


#### What are mandatory and optional parameters?

- Should be decide based on requirement/functionality.
- Example
    - In Employee class
    - Id, name are mandatory fields
    - Mobile, PAN, address, accountNoetc ., are optional fields.


### Constructor Overloading - Example


# QUIZ


- What is inheritance?


- **Inheritance** is a mechanism wherein a new class is derived from an
    existing class.


- What is Encapsulation?


- **Encapsulation** in **Java** is a mechanism of wrapping the data and
    methods together as a single unit


- How can we achieve Encapsulation in java?


- By using class with proper access specifiers


- How can we achieve abstraction in java?


- Using Interfaces and Abstract Classes


# MR


### Assignment -I

- Create Employee class with id, name and properties.
- Generate 3 parameter constructor.
- Generate getter/setter method for each property.
- Create EmployeeTest Class
    - In main method
       - Create Employee instance by providing all 3 properties
       - Display the same.


### Assignment –II (Understanding Aggregation)

- Create Address class with hno, street, city and pincode.
- Generate constructor with all the fields.
- Declare instance of Address class in Employee class
- Generate getter/setter methods for address in Employee Class
- In EmployeeTest Class
    - In main method
       - Create Address instance
       - Set the address to employee
       - Display employee and address details.


### Assignment – III ( Understanding Inheritance)

- Create ContractEmployee with one property called tenure
- Generate getter/setter method
- extend Employee ( public class ContractEmployee extends Employee)
- In EmployeeTest Class
    - In main method
       - Declare Employee instance and point to ContractEmployeeinstance
       - Create Address instance and set the details
       - Set address to contractEmployeeobject
       - Display employee and address details


