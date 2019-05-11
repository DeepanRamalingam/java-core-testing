---
layout: main
title: IO Streams
previousLink: ./multithreaded-programming-in-java
previousTitle: Multithreaded Programming in Java
duration: 
---

# IO Streams  

#### Objectives

- To understand the principles of I/O streams and where to

```
use them
```
- To understand the options and limitations of I/O streams
- To become comfortable with the mechanisms for accessing the file

system


#### What is Stream?

- A Stream is a sequential flow of data.
- Streams are like one way streets.
    - Input streams are for reading.
    - Output streams are for writing.


#### Input – Output Streams


#### Java Stream - Types

```
8 bits 16 bits
```

### Byte Oriented Streams

- Will discuss
    - Built-in classes
    - Methods
    - examples


#### Class Hierarchy


##### InputStream Methods


#### OutputStream Methods


#### Copy file from source to destination


### Character Oriented Streams

- Will discuss
    - Built-in classes
    - Methods
    - examples


#### Class Hierarchy


#### Methods available in Reader


#### Methods available in Reader


#### Reading from a file


#### Copy file – using Reader/Writer


# The File Class


#### The File Class

- An abstract representation of file and directory pathnames.


#### File class Constructor

- **File(File parent, String child) :** Creates a new File instance from a
    parent abstract pathname and a child pathname string.
- **File(String pathname) :** Creates a new File instance by converting the
    given pathname string into an abstract pathname.
- **File(String parent, String child) :** Creates a new File instance from a
    parent pathname string and a child pathname string.
- **File(URI uri) :** Creates a new File instance by converting the given file:
    URI into an abstract pathname.


#### Few File class methods

- **boolean canRead()** : Tests whether the application can read the file
    denoted by this abstract pathname.
- **boolean canWrite() :** Tests whether the application can modify the
    file denoted by this abstract pathname.
- **boolean createNewFile() :** Atomically creates a new, empty file
    named by this abstract pathname.
- **static File createTempFile(String prefix, String suffix) :** Creates an
    empty file in the default temporary-file directory.


#### Few File class methods

- **String getPath() :** Converts this abstract pathname into a pathname
    string.
- **boolean isDirectory() :** Tests whether the file denoted by this
    pathname is a directory.
- **boolean isFile() :** Tests whether the file denoted by this abstract
    pathname is a normal file.
- **boolean isHidden() :** Tests whether the file named by this abstract
    pathname is a hidden file.
- **long length() :** Returns the length of the file denoted by this abstract
    pathname.


#### Few File class methods

- **boolean mkdir() :** Creates the directory named by this abstract
    pathname.
- **boolean renameTo(File dest) :** Renames the file denoted by this
    abstract pathname.


#### Few File class methods

- **boolean delete() :** Deletes the file or directory denoted by this abstract
    pathname.
- **boolean exists()** : Tests whether the file or directory denoted by this abstract
    pathname exists.
- **String getAbsolutePath() :** Returns the absolute pathname string of this abstract
    pathname.
- **long getFreeSpace() :** Returns the number of unallocated bytes in the partition.
- **String getName() :** Returns the name of the file or directory denoted by this
    abstract pathname.
- **String getParent() :** Returns the pathname string of this abstract pathname’s
    parent.
- **File getParentFile() :** Returns the abstract pathname of this abstract pathname’s
    parent.


#### File Class Example


# QIUZ


- What is a stream


- A Stream is a sequential flow of data.
- Streams are like one way streets.
    - Input streams are for reading.
    - Output streams are for writing.


- What are the interfaces available in Character oriented and Byte
    oriented streams?


- Character Oriented
    - Reader
    - Writer
- Byte Oriented
    - InputStream
    - OutputStream


# MR


#### Practice Exercises.

- Write a function to copy a file from one location to another using
    - Character oriented stream
    - Byte oriented stream.
- Write a function to get specific files by extensions from a specified
    folder.
- Write a function to read first line from csv file.
- Writer a function to read content except first line from csv file.


