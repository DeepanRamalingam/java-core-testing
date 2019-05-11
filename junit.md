---
layout: main
title: JUnit
previousLink: ./assertions
previousTitle: Assertions
nextLink: ./exceptional-handling
nextTitle: Exceptional Handling
duration: 
---

# JUnit  

### Objectives

- What is Unit Testing?
- What is JUnit?
- Creating JUnit Testcase in Eclipse
- Creating simple JUnit Test cases
- JUnit Testcase result/output
- Basic Annotations in JUnit
- List of the assert methods with examples


### What is Unit Testing?

- **UNIT TESTING** is a level of software **testing** where individual units/
    components of a software are tested.
- The purpose is to validate that each **unit** of the software performs as
    designed.
- A **unit** is the smallest testable part of any software. It usually has one
    or a few inputs and usually a single output.


### What is Junit?

- JUnit is an open source Unit Testing Framework for JAVA.
- It is useful for Java Developers to write and run repeatable tests.


### Creating JUnit Testcase in Eclipse

1)Right click on the package
where you want to create
JUnitTest case
2) Choose JunitTest Case Option


### Creating JUnit Testcase in Eclipse

3)Select New JUnit4 test
4)Give the name of test case
Note: Better the test case name
end with TestCase


### Creating Junit Testcase in Eclipse

5)Adding Junit4 build path
Select –Perform the following action


### Generated Code in JUnit Test Class

```
The code which is generated as follows
You can run as JunitTest case
```

### JUnit Test Case – Example - I

```
Write a simple method called add in the class
We have to test whether this method is working fine or not with JUnitTest case
```

### JUnit Test Case – Example - I


### Running JUnit Testcase in eclipse


### JUnit Testcase result/output

- The Testcase may
    - Pass (Green right mark)
    - Fail (Blue cross mark)
    - Throw exception(Red cross mark)


### Basic Annotations in JUnit

- @Test
- @Before
- @BeforeClass
- @After
- @AfterClass
- @Ignore:


### Basic Annotations in JUnit

- @Test : To make the method as test case.
- @Before :
    - This annotation is used if you want to execute some statement such as
       preconditions **before each test case**.
    - Used to reinitialize the objects each time before executing each Testcase
- @BeforeClass
    - This annotation is used if you want to execute some statements **before all the**
       **test cases**
    - Used to initialize the objects etc.,


### Basic Annotations in JUnit

- @After :
    - This annotation can be used if you want to execute some statements after
       each Test Casefor e.gresetting variables, deleting temporary files ,variables,
       etc
- @AfterClass
    - This annotation can be used if you want to execute some statements after all
       test cases for e.g. Releasing resources after executing all test cases.


### Basic Annotations in JUnit

- @Ignore:
    - This annotation can be used if you want to ignore some statements during
       test execution for e.g. disabling some test cases during test execution.
- @Test(timeout=some value)
    - This annotation can be used if you want to set some timeout during test
       execution
- @Test(expected=SomeException.class)
    - This annotation can be used if you want to handle some exception during test
       execution.


### JUnit Test Case – Example - II


### JUnit Test Case – Example - II


### JUnit Test Case – Example - II


### JUnit Test Case Result

- The testcasemay
    - Pass (Green right mark)
    - Fail (Blue cross mark)
    - Throw exception(Red
    cross mark)

Passed

```
Failed
Reason why it is failed
```

### List of the assert methods:

- **assertEquals()**
- **assertTrue() + assertFalse()**
- **assertNull() + assertNotNull()**
- **assertSame() + assertNotSame()**
- **assertArrayEquals()**
- **assertThat()**


#### assertEquals()

- The assertEquals() method compares two objects for equality, using
    their equals() method.


#### assertTrue() + assertFalse()

- The assertTrue() and assertFalse() methods tests a single variable to
    see if its value is either true, or false.


#### assertTrue() + assertFalse()

#### Example


#### assertNull() + assertNotNull()

- The assertNull() and assertNotNull() methods test a single variable to
    see if it is null or not null.


#### assertSame() and assertNotSame()

- The assertSame() and assertNotSame() methods tests if two object
    references point to the same object or not. It is not enough that the
    two objects pointed to are equals according to
    their equals() methods. It must be exactly the same object pointed to.


### assertArrayEquals()

- The assertArrayEquals() method will test whether two arrays are
    equal to each other.
- In other words, if the two arrays contain the same number of
    elements, and if all the elements in the array are equal to each other.
- To check for element equality, the elements in the array are
    compared using their equals() method.
- More specifically, the elements of each array are compared one by
    one using their equals() method.
- That means, that it is not enough that the two arrays contain the
    same elements.
- They must also be present in the same order.


### Other Examples


# QUIZ


- What is JUnit?


- JUnit is an open source Unit Testing Framework for JAVA.


- What are the basic annotations in JUnit?


- @Test
- @Before
- @BeforeClass
- @After
- @AfterClass
- @Ignore:


- What is the difference between @Before and @BeforeClass?


- @Before
    - is used if you want to execute some statement such as preconditions **before**
       **each test case**.
    - Will execute multiple times, before executing each test case
- @BeforeClass
    - is used if you want to execute some statements **before all the test cases**
    - Will execute only once.


# MR


### Exercises

- Write the following functions and test with Junit Test cases
    - Write a function to get biggest between 2 numbers.
    - Write a function to find whether given number is prime or
    - Write a function to find whether the given string is palindrome or not.
    - Write a function to get sum of all the numbers in the given array