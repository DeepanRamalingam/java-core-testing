---
layout: main
title: Multithreaded Programming in Java
previousLink: ./enumeration
previousTitle: Enumeration
nextLink: ./io-streams
nextTitle: IO Streams
duration: 
---

# Multithreaded Programming in Java  

### Objectives

- Flow of single threaded program
- Flow of Multithreaded Program
- What are Threads?
- Threading Mechanisms
    - Extending Thread
    - Implementing RunnableInterface
- Thread life cycle
- Thread class API
- Shared Resource
- Need of Thread Safety
- Thread Priority
- The volatile keyword
- AutomicOperations in Java


### A single threaded program

class ABC

{

....

```
public void main(..)
{
...
..
}
```
}

```
begin
```
```
body
```
```
end
```

### A Multithreaded Program

```
Main Thread
```
Thread A Thread B Thread C

```
start start
```
```
start
```
```
Threads may switch or exchange data/results
```

### What are Threads?

 A piece of code that run in concurrent with other threads.

 Each thread is a statically ordered sequence of instructions.

 Threads are being extensively used express concurrency on both
single and multiprocessors machines.

 Java Threads are managed by JVM


### Threading Mechanisms...

 Create a class that extends the Thread class

 Create a class that implements the Runnable interface


##### 1st method: Extending Thread class

 Threads are implemented as objects that contains a
method called run()
class MyThread extends Thread
{
public void run()
{
// thread body of execution
}
}
 Create a thread:
MyThread thr1 = new MyThread();
 Start Execution of threads:
thr1.start();


###### 2nd method: Threads by implementing

###### Runnable interface

class MyThread implements Runnable
{
.....
public void run()
{
// thread body of execution
}
}
 Creating Object:
MyThread myObject = new MyThread();
 Creating Thread Object:
Thread thr1 = new Thread( myObject );
 Start Execution:
thr1.start();


### Example – extend Thread class


### Example – implementing Runnable interface


### Implements Runnable Vs extends Thread


### Thread Life Cycles – Different States of Thread


### Objectives

- Flow of single threaded program
- Flow of Multithreaded Program
- What are Threads?
- Threading Mechanisms
    - Extending Thread
    - Implementing RunnableInterface
- Thread life cycle
- Thread class API
- Shared Resource
- Need of Thread Safety
- Thread Priority
- The volatile keyword
- AutomicOperations in Java


# Thread Class API


#### Thread Class API

- run()
    - If this thread was constructed using a separate Runnable run object, then
       thatRunnable object's runmethod is called;
    - otherwise, this method does nothing and returns.
- start()
    - Causes this thread to begin execution; the Java Virtual Machine calls
       therunmethod of this thread.
- setName(Stringname)
    - Changes the name of this thread to be equal to the argument name.
- getName()
    - Returns this thread's name.
- getId()
    - Returns the identifier of this Thread.


### Thread Class API

- getPriority()
    - Returns this thread's priority.
- setPriority(intnewPriority)
    - Changes the priority of this thread.
- getState()
    - Returns the state of this thread.
- Ex: NEW, RUNNABLE, TERMINATED
- isAlive()
    - Tests if this thread is alive.


### Thread Class API

- isDaemon()
    - Tests if this thread is a daemon thread.
- setDaemon(booleanon)
    - Marks this thread as either a daemonthread or a user thread.


### Thread Class API

- join()
    - Waits for this thread to die.
- join(longmillis)
    - Waits at mostmillismilliseconds for this thread to die.
- join(longmillis, int nanos)
    - Waits at mostmillismilliseconds plusnanosnanoseconds for this thread to die.


### Thread Class API

- sleep(longmillis)
    - Causes the currently executing thread to sleep (temporarily cease execution) for the specified
       number of milliseconds, subject to the precision and accuracy of system timers and
       schedulers.
- sleep(longmillis, int nanos)
    - Causes the currently executing thread to sleep (temporarily cease execution) for the specified
       number of milliseconds plus the specified number of nanoseconds, subject to the precision
       and accuracy of system timers and schedulers.


### Thread Class API

- currentThread()
    - Returns a reference to the currently executing thread object.
- Destroy() && resume()
    - Deprecated.
    - This method was originally designed to destroy this thread without any cleanup.
    - This method was never implemented.
    - If it were to be implemented, it would be deadlock-prone in much the manner ofsuspend().
       If the target thread held a lock protecting a critical system resource when it was destroyed,
       no thread could ever access this resource again.


### Printing Mathematical table


### Thread.sleep Example


#### Multi thread example – execute sequential?

```
Time slicing : A task executes for a predefined slice of
time and then reentersthe pool of ready tasks.
The scheduler then determines which task should
execute next, based on priority and other factors.
```

- How to wait till completion of the task1 and start task 2?


- How to wait till completion of the task1 and start task 2?
- You can use join method
- Can use synchronized key word(will discuss later)


### Thread – join example


### Objectives

- Flow of single threaded program
- Flow of Multithreaded Program
- What are Threads?
- Threading Mechanisms
    - Extending Thread
    - Implementing RunnableInterface
- Thread life cycle
- Thread class API
- Shared Resource
- Need of Thread Safety
- Thread Priority
- The volatile keyword
- AutomicOperations in Java


# Shared Resources

# and

# Thread Safety



### Shared Resources

 If one thread tries to read the data and other thread
tries to update the same date, it leads to
inconsistent state.

 This can be prevented by synchronising access to
data.

 In Java: “Synchronized” method:

```
 syncronised void update()
 {
 ...
 }
```

##### Threads sharing the same object

class InternetBankingSystem {
public static void main(String [] args ) {
Account accountObject= new Account ();
Thread t1 = new Thread(new
DepositThread(accountObject));
Thread t2 = new Thread(new
WithdrawThread(accountObject));
Thread t3 = new Thread(new
EnquiryThread(accountObject));
t1.start();
t2.start();
t3.start();
// DO some other operation
} // end main()
}


#### Program with 3 threads and

#### shared object

class DepositThreadimplements Runnable {
Accountaccount;
public DepositThread(Accounts) { account = s;}
public void run() { account.deposit(); }
} // end class DepositThread

class WithdrawThreadimplements Runnable {
Account account;
public WithdrawThread(Accounts) { account = s; }
public void run() { account.withdraw(); }
} // end class WithdrawThread

class EnquiryThreadimplements Runnable {
Account account;
public EnquiryThread(Account s) { account = s; }
public void run() {account.enquire(); }
} // end class EnquiryThread

###### accoun

###### t


### Monitor (shared object) example

```
class Account { // the 'monitor'
// DATA Members
intbalance;
// if 'synchronized' is removed, the outcome is unpredictable
public synchronizedvoid deposit( ) {
// METHOD BODY : balance += deposit_amount;
}
public synchronizedvoid withdraw( ) {
// METHOD BODY: balance -= deposit_amount;
}
public synchronizedvoid enquire( ) {
// METHOD BODY: display balance.
}
}
```

### Inter-thread Communication in Java


#### Inter-thread Communication in Java

- Java uses three methods, namely, **wait(), notify() and notifyAll().**
    All these methods belong to object class as final so that all classes
    have them.
- They must be used within a synchronized block only.
- **wait()-** It tells the calling thread to give up the lock and go to sleep
    until some other thread enters the same monitor and calls notify().
- **notify()-** It wakes up one single thread that called wait() on the same
    object. It should be noted that calling notify() does not actually give
    up a lock on a resource.
- **notifyAll()-** It wakes up all the threads that called wait() on the same
    object.


### Thread Priority

```
 In Java, each thread is assigned priority, which
affects the order in which it is scheduled for
running. The threads so far had same default
priority (ORM_PRIORITY) and they are served using
FCFS policy.
 Java allows users to change priority:
 ThreadName.setPriority(intNumber)
 MIN_PRIORITY = 1
 NORM_PRIORITY=5
 MAX_PRIORITY=10
```

### Volatile key word

- If a variable is declared with the _volatile_ keyword then it is guaranteed
    that any thread that reads the field will see the most recently written
    value.
- The _volatile_ keyword will not perform any mutual exclusive lock on
    the variable.


#### Atomic operation

- Assume i is defined as int.
- The i++ (increment) operation it not an atomic operation in Java.
- The i++ operation first reads the value which is currently stored in i
    (atomic operations) and then it adds one to it (atomic operation).
- But between the read and the write the value of i might have
    changed.
- How can we solve this issue? - How can we make it automic?


### AtomicInteger, AtomicLong etc.,

- Since Java 1.5 the java language provides atomic variables, e.g.
    AtomicInteger or AtomicLong which provide methods
    like getAndDecrement(), getAndIncrement() and getAndSet()which
    are atomic


# QUIZ


- What is Thread?


- A piece of code that run in concurrent with other threads.


- How can we create Threads in java?


- By extending Thread class
- By implementing Runnable interface


- How to lock resource in java


- By using synchronized key word


# MR


### Exercise

- Practice the threads by extending Thread and implementing Runnable
    interface.


### Exercise

- Write a program called MathsTable which print mathematical table of
    given number.
- From main class
    - Create one object of MathsTable and pass any of the number (say 5)
    - Try to print mathematical tables between 1 to 10


### Exercise

- Write a program called MyArray that find biggest number in the given
    array.
- In Main class
    - Create 4 Threads of MyArrayand pass different arrays.
    - Check the output by printing biggest number in each array.
- Check whether you are getting proper output or not.
- Hint : Use synchronized key word


