---
layout: main
title: Annotations
previousLink: ./generics
previousTitle: Generics
nextLink: ./assertions
nextTitle: Assertions
duration: 
---

# Annotations  

### Objectives

- What is Annotation?
- Usage of Annotations
- Built-In Java Annotations
- User define Annotations
- (Custom Annotations)
- Meta-Annotations
- Example – JPA Annotations
- Example – JUnit Annotations


### What is Annotation?

Java **Annotation** is a tag that represents the _metadata_ i.e. attached with class,
interface, methods or fields to indicate some additional information which can
be used by java compiler and JVM.


### Usage of Annotations

##### Annotations have a number of uses, among them:

```
Information for the compiler - Annotations can be used by the compiler to
detect errors or suppress warnings
Compiler-time and deployment-time processing - Software tools can process
annotation information to generate code, XML files, and so forth
Runtime processing - Some annotations are available to be examined at
runtime (reflection)
```

### Built-In Java Annotations

##### Built-In Java Annotations used in java code

##### @Override

##### @SuppressWarnings

##### @Deprecated


#### @Override (discussed in the previous session)


### @Override

- It is optional, but better to use it.
- If programmer makes any mistake such as wrong method name, wrong

###### parameter types while overriding, you would get a compile time error.

- As by using this annotation you instruct compiler that you are overriding

###### this method.

- If you don’t use the annotation then the sub class method would behave as

###### a new method (not the overriding method) in sub class.

- If you change the signature of overridden method then all the sub classes

###### that overrides the particular method would throw a compilation error,

###### which would eventually help you to change the signature in the sub

###### classes.


### @SuppressWarnings

##### is used to suppress warnings issued by the compiler.


### @SuppressWarnings


### @Deprecated

- @Deprecated annotation marks that this method is deprecated so

##### compiler prints warning.

- It informs user that it may be removed in the future versions.
- So, it is better not to use such methods.


### @Deprecated


### @Deprecated


# User define Annotations

# (Custom Annotations)


### User defined annotation

```
public @interface Interface_name {
}
```
```
public @interface Author {
intString name() default id(); “Stackroute";
} String date();
```
```
Syntax to create User defined Annotation
```
```
Example
```

### Annotation Type Declaration

Similar to normal interface declarations:

An at-sign @ precedes the interface keyword
Each method declaration defines an element of the annotation type
Methods can have default values
Once an annotation type is defined, you can use it to annotate declarations

```
public @interface Author {
intString synopsis();id();
String name() default String date(); “Stackroute";
}
```

### Annotating Declarations..

##### In annotations with a single element, the element should

##### be named value :

##### It is permissible to omit the element name and equals

##### sign (=) in a single-element annotation:

##### If no values, then no parentheses needed:

```
public @interface Copyright {
String value();
}
```
```
@Copyright(" 2018 Stackroute")
public class Employee { ... }
```

### What can be annotated?

##### Annotatable program elements:

```
package
class, including
interface
enum
method
field
only at compile time
local variable
formal parameter
```

### Meta-Annotations

**Meta-annotations** - types designed for annotating annotation-type declarations
(annotations-of-annotations)

Meta-annotations:
**@Target** - indicates the targeted elements of a class in which the annotation type will be
applicable

- TYPE, FIELD, METHOD, PARAMETER, CONSTRUCTOR, etc
**@Retention** - how long the element holds onto its annotation
- SOURCE, CLASS, RUNTIME
**@Documented** - indicates that an annotation with this type should be documented by the
javadoctool
**@Inherited** - indicates that the annotated class with this type is automatically inherited


### Annotation Processing

It's possible to read a Java program and take actions based on its annotations
To make annotation information available at runtime, the annotation type
itself must be annotated with **@Retention(RetentionPolicy.RUNTIME)** :

```
@Retention(RetentionPolicy.RUNTIME)
@interface AnnotationForRuntime {
} // Elements that give information for runtime processing
```

### Example – JPA Annotations

##### When using JPA, you can configure the JPA behavior of your entities

##### using annotations:

```
@Entity - designate a plain old Java object (POJO) class as an entity so that
you can use it with JPA services
@Table, @Column, @JoinColumn, @PrimaryKeyJoinColumn – database
schema attributes
@OneToOne, @ManyToMany – relationship mappings
@Inheritance, @DiscriminatorColumn – inheritance controlling
```

### Example – JUnit Annotations

##### Annotations and support for Java 5 are key new features of JUnit 4:

```
@Test – annotates test method
@Before, @After – annotates setUp() and tearDown() methods for each
test
@BeforeClass, @AfterClass – class-scoped setUp() and tearDown()
@Ignore – do not run test
```

# QUIZ


- What is an Annotation?


- Java **Annotation** is a tag that represents the _metadata_ i.e. attached

##### with class, interface, methods or fields to indicate some additional

##### information which can be used by java compiler and JVM.


- What is @Deprecated?


- @Deprecated annotation marks that this method is deprecated so

##### compiler prints warning.

- It informs user that it may be removed in the future versions.


# MR


### Exercise -I

- Understand @Override
    - Create an Interface called Account
    - Add 3 methods i.e., openAccount,closeAccountand getBalace
    - Create a class called SavingAccountwhich implements Account interface
    - Test it
    - Try to change the method name getBalance to getBalanceAmount
    - Are you getting compilation errors in SavingAccount
       - You will get, if you have added @Override annotation while implementing


### Exercise -II

- Understanding @SuppressWarning
    - Try to get current Date from the java.util.Date class
    - Check whether it is deprecated or not
    - Check whether compiler giving warnings or not?
       - Open problems tab in eclipse and see
    - Add @SuppressWarning
       - Check again.


### Exercise -III

- Userdefined Annotation
    - Create UserDefined annotation for javadoc
    - Generate javadoc and check


