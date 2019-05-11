---
layout: main
title: Working with Strings
previousLink: ./working-with-arrays
previousTitle: Working with Arrays
nextLink: ./java-collection-framework
nextTitle: Java Collection Framrwork
duration: 
---

# Working with Strings  

#### Objectives

- What is String
- How to create String object?
- String literal – facts
- String Class methods
- String Vs StringBuffer Vs StringBuilder
- Understanding Immutability
- Why Strings are immutable?


#### What is String?

string is basically an object that represents sequence of char values.

The String class belongs to the java.lang package, which does not
require an import statement.

Like other classes, String has constructors and methods.

Unlike other classes, String has two operators, + and += (used for
concatenation).


#### How to create String object?

- By string literal
- By new keyword


#### Creating String object

//By using string literal
String s1 = “Hello”

```
//By new key word
String s1 =new String( “Hello”);
```

#### String literal - facts

- Each time you use a string literal, the JVM checks the string constant
    pool first.
- If the string already exists in the pool, a reference to the pooled
    instance is returned.
- If string doesn't exist in the pool, a new string instance is created and
    placed in the pool


#### String Class methods

- **int length()** : It returns the length of a String.
- **char charAt(int index)** : It returns the character at the specified index.
    Specified index value should be between 0 to length() -1 both inclusive. It
    throws IndexOutOfBoundsException if index<0||>= length of String.
- **boolean equals(Object obj)** : Compares the string with the specified string
    and returns true if both matches else false.
- **boolean equalsIgnoreCase(String string)** : It works same as equals method
    but it doesn’t consider the case while comparing strings. It does a case
    insensitive comparison.
- **int compareTo(String string)** : This method compares the two strings based
    on the Unicode value of each character in the strings.
- **int compareToIgnoreCase(String string)** : Same as CompareTo method
    however it ignores the case during comparison.


#### String Class methods

- **boolean startsWith(String prefix, int offset)** : It checks whether the
    substring (starting from the specified offset index) is having the
    specified prefix or not.
- **boolean startsWith(String prefix)** : It tests whether the string is having
    specified prefix, if yes then it returns true else false.
- **boolean endsWith(String suffix)** : Checks whether the string ends
    with the specified suffix.
- **int hashCode()** : It returns the hash code of the string.
- **int indexOf(int ch)** : Returns the index of first occurrence of the
    specified character ch in the string.


#### String Class methods

- **int indexOf(int ch, int fromIndex)** : Same as indexOf method however
    it starts searching in the string from the specified fromIndex.
- **int lastIndexOf(int ch)** : It returns the last occurrence of the character
    ch in the string.
- **int lastIndexOf(int ch, int fromIndex)** : Same as lastIndexOf(int ch)
    method, it starts search from fromIndex.
- **int indexOf(String str)** : This method returns the index of first
    occurrence of specified substring str.
- **int lastindexOf(String str)** : Returns the index of last occurrence of
    string str.


#### String Class methods

- **String substring(int beginIndex)** : It returns the substring of the string. The
    substring starts with the character at the specified index.
- **String substring(int beginIndex, int endIndex)** : Returns the substring. The
    substring starts with character at beginIndex and ends with the character
    at endIndex.
- **String concat(String str)** : Concatenates the specified string “str” at the end
    of the string.
- **String replace(char oldChar, char newChar)** : It returns the new updated
    string after changing all the occurrences of oldChar with the newChar.
- **boolean contains(CharSequence s)** : It checks whether the string contains
    the specified sequence of char values. If yes then it returns true else false.
    It throws NullPointerException of ‘s’ is null.


#### String Class methods

- **String toUpperCase(Locale locale)** : Converts the string to upper case string
    using the rules defined by specified locale.
- **String toUpperCase()** : Equivalent to toUpperCase(Locale.getDefault()).
- **public String intern()** : This method searches the specified string in the
    memory pool and if it is found then it returns the reference of it, else it
    allocates the memory space to the specified string and assign the reference
    to it.
- **public boolean isEmpty()** : This method returns true if the given string has 0
    length. If the length of the specified Java String is non-zero then it returns
    false.
- **public static String join()** : This method joins the given strings using the
    specified delimiter and returns the concatenated Java String


#### String Class methods

- **public static String format()** : This method returns a formatted java
    String
- **String toLowerCase()** : Equivalent to toLowerCase(Locale.
    getDefault()).
- **String trim()** : Returns the substring after omitting leading and trailing
    white spaces from the original string.
- **char[] toCharArray()** : Converts the string to a character array.
- **static String copyValueOf(char[] data)** : It returns a string that
    contains the characters of the specified character array.


#### String Class methods

- **static String copyValueOf(char[] data, int offset, int count)** : Same as above
    method with two extra arguments – initial offset of subarrayand length of
    subarray.
- **void getChars(int srcBegin, int srcEnd, char[] dest, int destBegin)** : It copies
    the characters of **src** array to the **dest** array. Only the specified range is
    being copied(srcBegin to srcEnd) to the dest subarray(starting
    fromdestBegin).
- **static String valueOf()** : This method returns a string representation of
    passed arguments such as int, long, float, double, char and char array.
- **boolean contentEquals(StringBuffer sb)** : It compares the string to the
    specified string buffer.
- **boolean regionMatches(int srcoffset, String dest, int destoffset, int len)** : It
    compares the substring of input to the substring of specified string.


### String

### String Buffer

### String Builder


#### String Vs StringBuffer Vs StringBuilder


#### Immutability

Once created, a string cannot be changed: none of its methods changes
the string.

Such objects are called _immutable_.

Immutable objects are convenient because several references can point
to the same object safely: there is no danger of changing an object
through one reference without the others being aware of the
change.


#### Advantages Of Immutability

Uses less memory.

```
String word1 = "Java";
String word2 = word1;
```
```
String word1 = “Java";
String word2 = new String(word1);
```
```
word
```
```
OK
```
```
Less efficient:
wastes memory
```
```
“Java"
```
```
“Java"
```
```
“Java"
word
```
```
word
```
```
word
```

#### Disadvantages of Immutability

```
Less efficient —you need to create a new string and throw
away the old one even for small changes.
```
```
String word = “Java";
word = word + “Tech”;
```
```
word “Java"
```
```
“Java Tech"
```

#### Why Strings are immutable?

- Requirement of String Pool
- Security
- Performance (multithread)
- Class Loader
- Cashe - hashcode value - performance


#### String constant pool

- String pool is possible only because String is immutable in java, this
    way Java Runtime saves a lot of java heap space because different
    String variables can refer to same String literal in the pool.
- If String would not have been immutable, then String interning would
    not have been possible because if any variable would have changed
    the value, it would have been reflected to other variables also.


#### Security

- f String is not immutable then it would cause severe security threat to
    the application.
- For example, database username, password are passed as String to
    get database connection and in socket programming host and port
    details passed as String.
- Since String is immutable it’s value can’t be changed otherwise any
    hacker could change the referenced value to cause security issues in
    the application.


#### Multithreading - performance

- Since String is immutable, it is safe for multithreading and a single
    String instance can be shared across different threads.
- This avoid the usage of synchronization for thread safety, Strings are
    implicitly thread safe.


#### Class loader

- Strings are used in java classloader and immutability provides security
    that correct class is getting loaded by Classloader.
- For example, think of an instance where you are trying to load
    java.sql.Connection class but the referenced value is changed to
    myhacked.Connection class that can do unwanted things to your
    database.


#### Cashing - hashCode

- Since String is immutable, its **hashCode** is cached at the time of
    creation and it doesn’t need to be calculated again.
- This makes it a great candidate for key in a Map and it’s processing is
    fast than other HashMap key objects.
- This is why String is mostly used Object as HashMap keys.


# Quiz


#### Quiz#1

- What does the String class have that other classes do not have?


- + and += operators and literal strings


#### Quiz#2

- What does **s.toUpperCase()** do to **s**?


- Nothing: s is immutable.


##### What is the output of each statement?


#### Output


# MR


#### Practice - Exercises

- Define generalized method to do the following functionality without
    using built-in String function
       - Find length of string
       - Compare whether two strings re equals or not
       - Check whether given string is palindrome or not
       - Find the number of occurrences of given character in given string.
       - Remove extra white spaces from the sentances. (only one white space
          between the words)
       - Simulate the trim function.


