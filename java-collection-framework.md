---
layout: main
title: Java Collection Framrwork
previousLink: ./working-with-strings
previousTitle: Working with Strings
nextLink: ./generics
nextTitle: Generics
duration: 
---

# Java Collection Framework  

### Objectives

- Collections: Aren't they just arrays?
- Introduction to Collections
- What is Collection Framework
- Core Collection Interfaces
- Collection Framework – Hierarchy
- The Collection Interface


### Objectives...

- Collection Interface
- Set Interface
- List Interface
- Map Interface
- Working with ArrayList
- Working with HashMap
- Which Collection I should use?


#### Collections: Aren't they just arrays?

In procedural languages, arrays are often the only way to represent
groups of data

Array provides a mechanism for memory management

Programmer must provide algorithms for managing the array

Arrays are, generally speaking, not Object Oriented

They are not cohesive

The array and the code to manage the array are not an single unit


### Introduction to Collections

A _collection_ — sometimes called a container — is simply an object that
groups multiple elements into a single unit.

Collections are used to store, retrieve, manipulate, and communicate
aggregate data.


### What is Collection Framework

A _collections framework_ is a unified architecture for representing and
manipulating collections.
All collections frameworks contain the following:
 **Interfaces:**. Interfaces allow collections to be manipulated
independently of the details of their representation. In object-
oriented languages, interfaces generally form a hierarchy.
 **Implementations:** These are the concrete implementations of the
collection interfaces. In essence, they are reusable data structures.
 **Algorithms:** These are the methods that perform useful
computations, such as searching and sorting, on objects that
implement collection interfaces.


### Core Collection Interfaces and Classes


### Methods in Collection Interface


### Methods in List Interface


### Working with ArrayList

- What is ArrayList
- How to create ArrayList
- Adding objects to ArrayList
- How to traverse ArrayList


### What is ArrayList

- The **ArrayList** class extends AbstractList and implements the List
    interface.
- **ArrayList** supports dynamic arrays that can grow as needed.


### Instantiating ArrayList


### Adding objects to ArrayList

```
Example 1 Example 2
```

### Traversing ArrayList

Example 1 Example 2


### Working with Map

- What is Map
- Methods in Map interface
- What is HashMap
- Instantiating HashMap
- Adding elements to HashMap
- Traversing HashMap


### What is Map?

- The **Map** Interface.
- A **Map** is an object that **maps** keys to values.
- A **map** cannot contain duplicate keys: Each key can **map** to at most
    one value. ...
- The **Java** platform contains **Map** implementations:
    - HashMap
    - TreeMap
    - LinkedHashMap.


### Methods in map interface


### What is HashMap

- **HashMap** class which implements implements the map interface.
- **HashMap** contains values based on the key.
- It contains only unique elements.
- It may have one null key and multiple null values


#### Instantiating HashMap


### Adding elements to HashMap


### Traversing HashMap


### Array Vs Collection

**Array Collection**
Arrays are fixed in size.Once we created an array we are not allowed to
increase or decrease the size. Collections are growrequirement we can increase or decrease the size.-able in nature and hence based on our
Arrays can hold both primitives as well as objects. Collections can hold only objects but not primitive.

Performance point of view arrays faster than collection Performance point of view collections are slower than array

Arrays can hold only homogeneous elements. Collections can hold both homogeneous and heterogeneous elements.
Memory point of view arrays are not recommended to use. Memory point of view collections are recommended to use.

We need to write our own code to implement functionality like insert, delete, search,sort etc., Built-in classes with algorithms are available.


### Which Collection I should use?


# QUIZ


- Is ArrayList allow Null values?


- Yes


- Is Set allow Duplicates?


- No


# MR


### ArrayList

- Write a methods to display all the elopements of ArrayList
    - Using while loop
    - Using Enhanced for loop
- Do the following operations
    - Insert an element at the end
    - Insert an element at the particular position
    - Delete an element
    - Get element from particular position
    - Merge two lists
    Note: use direct methods available in the List.


### ArrayList

- Create Employee Class with id, name and salary
- Create few Employee instances and add the list
- Write method to display all the employees
- Write method to get particular employee based on id.


### HashMap

- Create Employee Class with id, name and salary
- Create few Employee instances and add the map
- Write method to display all the employees
- Write method to get particular employee based on id
- Note: take employeedID as key and employee object as value.


