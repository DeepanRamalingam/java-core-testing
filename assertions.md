---
layout: main
title: Assertions
previousLink: ./annotations
previousTitle: Annotations
nextLink: ./junit
nextTitle: JUnit
duration: 
---

# Assertions  

### Objectives

- What is an assertion?
- Why to use assertions?
- Simple Assertion Form
- Complex Assertion Form
- Assertion Examples
- Performance Problems?
- Enable/Disable Assertion


#### What is an assertion?

 An _assertion_ is a statement in Java that enables you to test your
assumptions about your program.

 Each assertion contains a boolean expression that you believe will be
true when the assertion executes.

 By verifying that the boolean expression is indeed true, the assertion
confirms your assumptions about the behavior of your program,
increasing your confidence that the program is free of errors.


#### Why to use assertions?

 Programming by contract

 Pre-conditions

- Assert precondition as requirement of client

 Post-conditions

- Assert post-condition as effect of client method


### Simple Assertion Form

 The assertion statement has two forms

 The first is:

```
assert Expression1 ;
```
 Where _Expression1_ is a boolean expression

 When the system runs the assertion,
it evaluates _Expression1_ and if it is false throws an AssertionError
with no details


### Complex Assertion Form

 The second form of the assertion statement is:

```
assert Expression1 : Expression2 ;
```
 where:

- _Expression1_ is a boolean expression
- _Expression2_ is an expression that has a value
- It cannot invoke of a method that is declared void


#### Complex Assertion Form..

 The second form of the assertion statement is:

```
assert Expression1 : Expression2 ;
```
 where:

- _Expression1_ is a boolean expression
- _Expression2_ is an expression that has a value
- It cannot invoke of a method that is declared void


### Assertion – Example - I


### Assertion – Example - II

```
Will throw AssertionErrorif s1 is null
```

### Assertion – Example - II


### Assertion – Example - III


#### When an Assertion Fails

 Assertion failures are labeled in stack trace with the file and line
number from which they were thrown

 Second form of the assertion statement should be used in preference
to the first when the program has some additional information that
might help diagnose the failure


### Performance Problems

 Assertions may slow down execution—why?

 For example, if an assertion checks to see if the element to be
returned is the smallest element in the list, then the assertion would
have to do the same amount of work that the method would have to
do

 So, assertions may be enabled and disabled

 Assertions are, by default, disabled at run-time

 In this case, the assertion has the same semantics as an empty
statement


### Arguments

 no arguments
Enables or disables assertions in all classes except system classes
 _packageName_ ...
Enables or disables assertions in the named package and any
subpackages
 ...
Enables or disables assertions in the unnamed package in the
current working directory
 _className_
Enables or disables assertions in the named class


### Enabling Assertions

 To enable assertions at various granularities, use the -
enableassertions, or -ea, switch

 To disable assertions at various granularities, use the -
disableassertions, or -da, switch


# QUIZ


- What is an Assertion?


- An _assertion_ is a statement in Java that enables you to test your
    assumptions about your program.


- How to use assertion? - Syntax


- assert _Expression1_ ;
- OR
- assert _Expression1_ : _Expression2_ ;


- Is assertion slow down execution?


- Yes.


# MR


### Excercizes

- Write a function get element from the given array of given position.
    Make sure that it should not get ArrayIndexOutOfBoundsException.
- Write a function compare two Employee objects. Make sure tht it
    should not get NullPointerException.


