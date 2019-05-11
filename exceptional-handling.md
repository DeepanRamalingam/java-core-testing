---
layout: main
title: Exceptional Handling
previousLink: ./junit
previousTitle: JUnit
nextLink: ./enumeration
nextTitle: Enumeration
duration: 
---

# Exceptional Handling    

### Objectives

- What is an Exception?
- Why exceptions will occur?
- Why to handle exception?
- Types of Exception
- Exception class hierarchy
- Useful methods in Throwable Class
- What is an Error?
- Exceptional Handling key words
- Java 1.7 enhancements
- User Defined Exception


### Is helmet required always???


### YES- Always


### What Is an Exception?

- An exception is an **event** that occurs during the execution of a
    program that disrupts the normal flow of instructions.


### Why exceptions will occur

An exception can occur for many different reasons.
Examples:
Dividing a number by zero
A file that needs to be opened cannot be found.
A network connection has been lost in the middle of communications
or the JVM has run out of memory.
Calling method on null object.
Inserting/fetching value with index which does not exist.


### Why to handle exception?

- If an exception is raised, which has not been handled by programmer
    then program execution can get **terminated** and system prints **a non**
    **user friendly error message**.


### Types of Exception

- Checked Exception ( Compile time exception)
- UnChecked Exception (Run time exception)


### Checked Exceptions

Checked Exceptions are exceptional scenarios that we can anticipate in
a program and try to recover from it.

We should catch this exception and provide useful message to user and
log it properly for debugging purpose.

If we are throwing a checked exception:
we must catch it in the same method
or
we have to propagate it to the caller using throws keyword.


### Un-Checked Exceptions

Runtime Exceptions are cause by bad programming, for example trying
to retrieve an element from the Array.
We should check the length of array first before trying to retrieve the
element otherwise it might throw ArrayIndexOutOfBoundException
at runtime.
RuntimeException is the parent class of all runtime exceptions.
If we are throwing any runtime exception in a method, it’s not required
to specify them in the method signature throws clause.
Runtime exceptions can be avoided with better programming.


### Class Hierarchy


### Class Hierarchy


### Methods of Throwable class

**public String getMessage()** – This method returns the message String
of Throwable and the message can be provided while creating the
exception through it’s constructor.

**public String getLocalizedMessage()** – This method is provided so that
subclasses can override it to provide locale specific message to the
calling program.

Throwable class implementation of this method simply use
getMessage() method to return the exception message.


### Methods of Throwable class

**public synchronized Throwable getCause()** – This method returns the cause
of the exception or null id the cause is unknown.

**public String toString()** – This method returns the information about
Throwable in String format, the returned String contains the name of
Throwable class and localized message.

**public void printStackTrace()** – This method prints the stack trace
information to the standard error stream, this method is overloaded and
we can pass PrintStream or PrintWriter as argument to write the stack
trace information to the file or stream.


### Error

```
Errors are exceptional scenarios that are out of scope of application
and it’s not possible to anticipate and recover from them, for example
hardware failure, JVM crash or out of memory error.
```
That’s why we have a separate hierarchy of errors and we should not
try to handle these situations.

Some of the common Errors are
OutOfMemoryError
StackOverflowError.


### Exception handling Key words

#### try

#### catch

#### finally

#### throw

#### throws


### Try – catch - finally


### Try – catch – finally -- Flow


### Example


### throw - throws

- If a method does not handle a checked exception, throws key word
    should be used at the end of a method's signature.
- To explicitly throw the exception of a newly instantiated one or an
    exception that you just caught, we use throw keyword.


### Throw – throws - example


## User Defined Exceptions


### User Defined exceptions


#### Java SE 7 Exception - Enhancement

Multi-catch exceptions
try-with-resources


#### Nested Catch (Before 1.7)


### Nested Catch (1.7)


### Before Java 7


### Try-with-resources – java 1.7


- User Defined Exception ( along with throw and throws)



# QUIZ


- What is an exception?


- An exception is an **event** that occurs during the execution of a
    program that disrupts the normal flow of instructions.


- Differences between checked and unchecked exception?


- **Checked:** are the exceptions that are
    checked at compile time.
- If some code within a method throws a
    checked exception,then the method
    must either handle the exception or it
    must specify the exception
    using _throws_ keyword.
- Under the Exception class except
    RuntimeExceptionare checked exception
       - **Unchecked** are the exceptions that are not
          checked at compiled time
       - It is up to the programmers to be civilized,
          and specify or catch the exceptions.
       - In Java exceptions
          under _Error_ and _RuntimeException_ classes
          are unchecked exceptions, everything else
          under throwableis checked.


# MR


### Practice exercises

- Create an array with size as 10. Try to access index 10. Observe what
    exception you are getting and why? How to avoid it?
- Declare two strings objects with null. Try to compare with equals
    method. Observe what exception you are getting and why? How to
    avoid it?
- Create an user defined exception called InvalidAgeException
    - Write a method called vote(intage)
    - Through InvalidAgeExceptionexception if the age is < 18
    - Test vote method by passing 20 and then 15. Check whether exception is
       through for the input 15.


