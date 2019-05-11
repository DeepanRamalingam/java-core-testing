---
layout: main
title: Generics
previousLink: ./java-collection-framework
previousTitle: Java Collection Framrwork
nextLink: ./annotations
nextTitle: Annotations
duration: 
---

# Generics  


### Objectives

- Why Generics?
- Storing specific type in collection
- Casting –Compile time exception
- Generics with Class and Interfaces
- Creating generalized class
- Generics in Interfaces
- Generics Type Naming Conventions
- Generics in Methods and Constructors
- Generics Bounded Type Parameters
- Generic classes and subtyping
- Generics Wildcards
- Generics Upper Bounded Wildcard
- Generics Unbounded Wildcard
- Generics Lower bounded Wildcard


### Why Generics?

- Generics allows a type or method to operate on objects of various
    types while providing compile-time type safety, making Java a fully
    statically typed language.


### Why Generics?

Generics was added in Java 5 to provide

```
C ompile-time type checking
```
```
Removing risk of ClassCastException
```
The whole collection framework was re-written to use generics for
type-safety.


### ClassCastException

List list = new ArrayList();

list.add("abc");

list.add(new Integer(5)); //OK

for(Object obj: list){

String str=(String) obj; //type casting leading to ClassCastExceptionat runtime

}

Above code compiles fine but throws ClassCastException at runtime because we
are trying to cast Object in the list to String whereas one of the element is of type
Integer.


### Casting – Compile time exception

After Java 5, we use collection classes like below.

List<String> list1 = new ArrayList<String>();

list1.add("abc");

//list1.add(new Integer(5)); //compiler error

for(String str : list1){

//no type casting needed, avoids ClassCastException

}


### Generics with Class and Interfaces

We can define our own classes and interfaces with generics type.

A generic type is a class or interface that is parameterized over types.

We use angle brackets (<>) to specify the type parameter.


### Get/Set Old way


#### Set/Get – Generic way


### Generics in Interfaces


### Generics Type Naming Conventions

```
Usually type parameter names are single, uppercase letters to make it
easily distinguishable from java variables.
```
The most commonly used type parameter names are:

```
E – Element (used extensively by the Java Collections Framework, for
example ArrayList, Set etc.)
K – Key (Used in Map)
N – Number
T – Type
V – Value (Used in Map)
```

### Generics in Methods and Constructors

Sometimes we don’t want whole class to be parameterized, in that case
we can use generics type in methods also.

Since constructor is a special kind of method, we can use generics type
in constructors too.


### Generics in Methods and Constructors

Sometimes we don’t want whole class to be parameterized, in that case
we can use generics type in methods also.

Since constructor is a special kind of method, we can use generics type
in constructors too.


### Generics in Methods and Constructors


### Generics Bounded Type Parameters

Want to restrict the type of objects that can be used in the parameterized
type.
for example in a method that compares two objects and we want to make
sure that the accepted objects are Comparables.

To declare a bounded type parameter, list the type parameter’s name, followed
by the extends keyword, followed by its upper bound

Ex:

public static <T extends Comparable<T>> int compare(T t1, T t2){

return t1.compareTo(t2);

}


### Generics Bounded Type Parameters

Bounded type parameters can be used with methods as well as classes
and interfaces

Generics supports multiple bounds also, i.e <T extends A & B & C>. In this
case A can be an interface or class. If A is class then B and C should be
interfaces. We can’t have more than one class in multiple bounds


### Generic classes and subtyping

We can subtype a generic class or interface by extending or implementing it.

```
The relationship between the type parameters of one class or interface and the type
parameters of another are determined by the extends and implements clauses.
```
For example, ArrayList<E> implements List<E> that extends Collection<E>, so
ArrayList<String> is a subtype of List<String> and List<String> is subtype of
Collection<String>.

The subtyping relationship is preserved as long as we don’t change the type
argument, below shows an example of multiple type parameters.

interface MyList<E,T> extends List<E>{

}

The subtypes of List<String> can be MyList<String,Object>, MyList<String,Integer>
and so on.


### Generics Wildcards

Question mark (?) is the wildcard in generics and represent an
unknown type.

The wildcard can be used as the type of a parameter, field, or local
variable and sometimes as a return type.

```
We can’t use wildcards while invoking a generic method or
instantiating a generic class.
```

### Generics Wildcards


### Generics Upper Bounded Wildcard


### Generics Unbounded Wildcard

Sometimes we have a situation where we want our generic method to be working with all types, in
this case unbounded wildcard can be used. Its same as using <? extends Object>.

public void printData(List<?> list){

```
for(Object obj: list){
System.out.print(obj+ "::");
}
}
```
We can provide List<String> or List<Integer> or any other type of Object list argument to the
_printData_ method.
Similar to upper bound list, we are not allowed to add anything to the list.


### Generics Lower bounded Wildcard

Suppose we want to add Integers to a list of integers in a method, we can keep
the argument type as List<Integer> but it will be tied up with Integers
whereas List<Number> and List<Object> can also hold integers, so we can
use lower bound wildcard to achieve this.

We use generics wildcard (?) with **super** keyword and lower bound class to
achieve this

We can pass lower bound or any super type of lower bound as an argument in
this case, java compiler allows to add lower bound object types to the list.

public void addIntegers(List<? super Integer> list){

list.add(new Integer(50));

}


# QUIZ


- Why generics?


- Generics allows a type or method to operate on objects of various
    types while providing compile-time type safety, making Java a fully
    statically typed language.


# MR


### Practice - Exercises

- Write a generalized class and generalized setter/getter methods.
- Do the same with generics – understand the advantages.


