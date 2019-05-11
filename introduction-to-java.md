---
layout: main
title: Introduction to Java
nextLink: ./java-language-fundamentals
nextTitle: Java Language Fundamentals
duration: 
---

# Introduction to Java  

### Objectives

- What is Java
- Characteristics of Java
- Write once Run Anywhere (WORA)
- Java Architecture
- Understanding JDK – JRE – JVM


#### What is Java

Java Technology consists of:


- Java Language
- Java Platform
- Java Tools


### Java Language

- Java language is a general-purpose programming language.
- It can be used to develop software for
    - mobile devices,
    - browser-run applets,
    - games,
    - desktop,
    - enterprise (server-side),
    - and scientific applications.


### Java Platform

- Java platform consists of
    - Java virtual machine (JVM) responsible for hardware abstraction,
    - and a set of libraries that gives Java a rich foundation.


### Java Tools

- Java tools include
    - the Java compiler
    - as well as various other helper applications
       - that are used for day-to-day development (e.g. debugger).


### Characteristics of Java

**Platform independent:**  

Java programs use the Java virtual machine as abstraction and do not access the operating system directly. This makes Java programs highly portable.
A Java program (which is standard complaint and follows certain
rules) can run unmodified on all supported platforms, e.g. Windows
or Linux.

**Object-orientated programming language:**
Except the primitive data types, all elements in Java are objects.


**Strongly-typed programming language:**
Java is strongly-typed, e.g. the types of the used variables must be
pre-defined and conversion to other objects is relatively strict, e.g.
must be done in most cases by the programmer.

**Interpreted and compiled language:**
Java source code is transferred into the bytecode format which does
not depend on the target platform.
These bytecode instructions will be interpreted by the Java Virtual
machine (JVM).
The JVM contains a so called Hotspot-Compiler which translates
performance critical bytecode instructions into native code
instructions.

**Automatic memory management:**

Java manages the memory allocation and de-allocation for creating
new objects.
The program does not have direct access to the memory.
The so-called garbage collector deletes automatically objects to which
no active pointer exists.

**Dynamic**
Java can load application components at run-time even if it knows
nothing about them.
Each class has a run-time representation.

**Distributed**
Java comes with support for networking, as well as for invoking
methods on remote (distributed) objects through RMI.

#### Write once Run Anywhere (WORA)


#### Java Architecture


#### Understanding JDK – JRE – JVM


### Quiz


- What are the differences between JDK, JRE and JVM?
- Is JVM is Platform independent?
	- No. Each platform has their own JVM.
	- Java compiler is platform independent, not JVM

### Download and Install JDK and Eclipse

### (Latest stable version)

Download and Install JDK
[http://www.oracle.com/technetwork/java/javase/downloads/jdk10-](http://www.oracle.com/technetwork/java/javase/downloads/jdk10-)
downloads-4416644.html
Download eclipse
https://www.eclipse.org/downloads/
Note: Download eclipse EE version (Enterprise Edition)


### Java - Environment Setup(Windows)


### Java - Environment Setup(Windows)


### Test Your Environment

- Open DOS Command Prompt
- Check the java version


### Unknown OR Un recognize command?

- If it says java is unknown or un recognize commands, that means your
    java environment setup not done properly.
- Check the steps and redo properly.


### Using Eclipse

- Open the Eclipse
- Provide workspace name.
- Workspace holds group of projects.
- Note: Do not create workspace in eclipse folder or in C Drive.


### Welcome Page

It will open Welcome page
Close the welcome page
See the Project Explorer


### Creating Java Project

- Right click on project explorer area
- Click New
- Select Project


### Creating Java Project..

- Select Java Project
- Give project name
- Click Finish


### Creating Package

- What is Package?
- Package consist of group of related classes
- It is just like folder which contains group of files
- Naming convention
    - <organization_type>.<organization_name>.<project_name>.<module_name>
- Example
    - com.stackroute.shoppingcart.controller
    - com.stackroute.shoppingcart.model


### How to create package?

- Right click on src folder
- Click New
- Select Package


### Create a Java Class

- Right on the package which you created
- Select Class
- Provide Class Name.
- Click Finish


- Select the class in project explorer


### Generate main method

- Type main
- Press Ctrl+space bar
- Select main method
- It will generate the code


### Generate System.out.println

- Type syso within main method
- Press Ctrl+space bar
- Will generate code


- Type Hello World! Within quotations


### Execute java program in eclipse

- Right click on the file
- Select Run As
- Select Java Application

```
See the output in console tab
```

### Practice..

- Practice by print some other text like (hard coded values)
- Address – H.No, street, city, pin code etc.,
- Student name, marks etc.,
- Employee id, name salary etc.,
- Will discuss what about main method
- And
- System.out.println later

