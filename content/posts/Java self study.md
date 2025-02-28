---
title: Java self study
date: 2025-02-27
tags:
  - BS_degree
  - Study
---
# Java Quiz 1 study

## The History and Evolution of Java
- Many features of Java are influenced by C and C++
- Invented and first implemented by Dennis Ritchie on the UNIX operating system, C was the result of a development process that started with an older language called BCPL, developed by Martin Richards. BCPL influenced a language called B, invented by Ken Thompson, which led to the development of C in the 1970s.
- C++ was invented by Bjarne Stroustrup in 1979, while he was working at Bell Laboratories in Murray Hill, New Jersey. Stroustrup initially called the new language “C with Classes.” However, in 1983, the name was changed to C++. C++ extends C by adding object-oriented features. Because C++ is built on the foundation of C, it includes all of C’s features, attributes and benefits
- Java was conceived by James Gosling, Patrick Naughton, Chris Warth, Ed Frank, and Mike Sheridan at Sun Microsystems, Inc. in 1991. It took 18 months to develop the first working version. This language was initially called “Oak,” but was renamed “Java” in 1995.
- Computer languages evolve for two reasons: to adapt to changes in environment and to implement advances in the art of programming.

**JVM** : Java Virtual Machine  
**JRE** : Java Runtime Environment  
The output of a Java compiler is not executable code. Rather, it is bytecode. Bytecode is a highly optimized set of instructions designed to be executed by what is called the Java Virtual Machine (JVM), which is part of the Java Runtime Environment (JRE). In essence, the original JVM was designed as an interpreter for bytecode.
> our code > compile > bytecode > run > result

### There are 4 types of applications we can create using Java.
1. **Stand Alone** : Desktop applications
2. **Web application** : runs on server side and create dynamic pages.
3. **Enterprise Application** : Distributed in nature, banking etc.
4. **Mobile Application** : Mobile games etc.
### 12 main characteristics of Java
1. **Simple** : Simple to learn, based on C++
2. **Object Oriented** : Everything in java is an object. In object oriented programming, we organize our software as a combination of different types of objects.
3. **Platform independent** : You can use Java on any platform : mac, Windows, Linux.
   1. There are two type of platforms : hardware based and software based. Java works on software based platform.
4. **Secured** : java programs run inside a virtual machine sandbox.
5. **Robust** : Strong memory management.
6. **Architectural - Neutral** : No implementation dependent features.
7. **Portable** : You can carry Java bytecode to any platform.
8. **High Performance** : java is faster than many languages. But slower than C++. because Java is an interpreted language, which are slower than compiled languages (C++).
   1. A **compiler** translates the entire source code into machine code than executes it. Results in faster execution.
   2. **Interpreter** translate code line by line during execution. making it easier to detect errors but slows down program.
9. **Interpreted**
10. **Distributed** : It facilitates users to create distributed applications in Java.
11. **Multi-threaded** : Java can deal with many tasks at once by defining multiple threads.
12. **Dynamic** : It supports dynamic loading of classes

## week 1
- **High level language** : Human readable
- **Low level language** : machine readable.
  - We need Compilers and interpreters to translate High level language to low level language.
  
- Abstractions used in computation thinking
	An essential element of object-oriented programming is abstraction. Humans manage complexity through abstraction. For example, people do not think of a car as a set of tens of thousands of individual parts. They think of it as a well-defined object with its own unique behavior. This abstraction allows people to use a car to drive to the grocery store without being overwhelmed by the complexity of the individual parts. They can ignore the details of how the engine, transmission, and braking systems work. Instead, they are free to utilize the object as a whole.
	
- compilers, interpreters
	   1. A **compiler** translates the entire source code into machine code than executes it. Results in faster execution.
		2. **Interpreter** translate code line by line during execution. making it easier to detect errors but slows down program
		- java is faster than many languages. But slower than C++. because Java is an interpreted language, which are slower than compiled languages (C++).  Python is also an interpreted language.
		
### 1. Imperative
   1. How to compute
   2. Step by step instructions
   3. Intermediate steps are given. whole process is given
### 2. Declarative
   1. What to compute
   2. Not much instructions
   3. Intermediate steps are not given
   4. Combination of small - small functions : Functional programming. Reccursion is also there
   
- collections
	- arrays, lists, dictionaries
	- stack : push and pop
	- queue : enqueue, dequeue
	
- Data Types
- Static vs dynamic typing 
	- Dynamic : you can set x value then you can change x value. you can change data types also. machine judges type on the basis of value. It can be changeable. If I defined x as int first. but then change it in float. it'll be fine.
	- Static : Associate data type with variable in advance, can't assisgn different data type value. With variable declaration  compilers can detect type errors at compile time.
	 - It's mandatory in java to define the type of our variable when we initiate our variable.
	
### Something about storage :
5 different places to store data
1. Registers. This is the fastest storage because it exists in a place different from that of
other storage: inside the processor. However, the number of registers is severely
limited, so registers are allocated as they are needed. You don’t have direct control,
nor do you see any evidence in your programs that registers even exist (C & C++, on
the other hand, allow you to suggest register allocation to the compiler).
2. The stack. This lives in the general random-access memory (RAM) area, but has
direct support from the processor via its stack pointer. The stack pointer is moved
down to create new memory and moved up to release that memory. This is an
extremely fast and efficient way to allocate storage, second only to registers. The Java
system must know, while it is creating the program, the exact lifetime of all the items
that are stored on the stack. This constraint places limits on the flexibility of your
programs, so while some Java storage exists on the stack—in particular, object
references—Java objects themselves are not placed on the stack.
3. The heap. This is a general-purpose pool of memory (also in the RAM area) where all
Java objects live. The nice thing about the heap is that, unlike the stack, the compiler
doesn’t need to know how long that storage must stay on the heap. Thus, there’s a
great deal of flexibility in using storage on the heap. Whenever you need an object, you
simply write the code to create it by using new, and the storage is allocated on the
heap when that code is executed. Of course there’s a price you pay for this flexibility: It
may take more time to allocate and clean up heap storage than stack storage (if you
even could create objects on the stack in Java, as you can in C++).
4. Constant storage. Constant values are often placed directly in the program code,
which is safe since they can never change. Sometimes constants are cordoned off by
themselves so that they can be optionally placed in read-only memory (ROM), in
embedded systems.2
5. Non-RAM storage. If data lives completely outside a program, it can exist while the
program is not running, outside the control of the program. The two primary
examples of this are streamed objects, in which objects are turned into streams of
bytes, generally to be sent to another machine, and persistent objects, in which the
objects are placed on disk so they will hold their state even when the program is
terminated. The trick with these types of storage is turning the objects into something
that can exist on the other medium, and yet can be resurrected into a regular RAM-
based object when necessary. Java provides support for lightweight persistence, and
mechanisms such as JDBC and Hibernate provide more sophisticated support for
storing and retrieving object information in databases.





- Scope of a variable : Local and global
- lifetime of a variable
    - How long a variable can stays in memory
	- In case of local variable, scope and lifetime are same.
- Memory stack
	- function needs storage for local variable
	- create activation record when function is called
		- activation records are stacked,  popped when function exits
		- link points to start of previous record
	- scope of variable
	- lifetime of a variable
- arguments : formal parameters
	- activation record
	- 2 ways to initialize the parameters
		- call by value
		- call by reference
- heap : linked list has some drawbacks
	- separate storage for persistent data : dynamically allocated vs statically declared
	- called Heap : (different from DSA)
	- Heap is at the opposite end of the stack
- Manual memory management
	- request and return heap storage
	- error prone
	- explicit deallocation
- Automatics garbage collection
	- mark and sweep
	
- Stepwise refinement
	- you can divide your problem in many subparts and many people can work on different parts. later you can combine them.
  - Dividing the program and then merging the solution.
	- start with a high level, then refine task into subtasks
	- again sub division
	- sub tasks or sub divisons can be coded by different people
	- program refine ment : focus on code not on data structure
	- top down, bottom up
- modular software developement
	- use refinement to divide the solution into components
	- build prototype for each component
	- components
		- interface : what is visible to others components, e.g. function calls
		- specifications : behaviour of component, as visible through interface
- control abstraction
	- Encapsulation
- data abstraction

- object oriented programming
- object is like an abstract datatype
- uniform way to encapsulating different combinations of data and functionality
	- an object can hold single integer or entire databse too
- features in object oriented programming
	- abstraction
	- subtyping
	- dynamic lookup
	- inheritance
- abstraction
	- objects are similar to abstract datatypes
	- data centric view of programming
	- recall stepwise refinement
- Subtyping
	- recall event queue
	- arrange types in hierarchy
- Dynamic lookup
	- type checking
	- how to method act is a dynamic property how the object is implemented
	- different from overloading
- inheritance
	- re-use of implementations
	- employee objects, manager objects
- difference between subtyping and inheritance. 
- deque is a double ended queue

- objects
- class
- constructor
- adding method to a class
- changing the internal implementations
- abstraction
how to use above concepts in coding

## week 2
- print command
- visibility
- availablity
- public class
- work of JVM and "write once run anywhere"
- javac

- scalar type
- IN OBJECT ORIENTED, ALL DATA SHOULD BE ENCAPSULATED AS OBJECTS
- 8 primitive scalar types and their size in bytes
	- int	4 bits
	- long	8
	- short	2
	- byte		1
	- float	4 bytes = 32 bits 
	- double	8 bytes = 64 bits
	- char		2 for Unicode
	- boolean	1, true false (in small)
- Declaration, assigining values
- initialization, constants
- airthmatic concepts
- Math.ppow()
- string in double quotes "string"
- method substing in class string
- Array are also objects
	- length
	- indices

- control flow
	- if else
		- but no elif
	- while
	- do, while
	- for : 2 types of for
	- multibranching : switch
	- iteration
	- break
	
- java classes
	- defining a class
	- instance variable
	- creating objects
	- new,this,
	- Accessor, Mutator methods
	- constructors
	- copy constructors
		- shallow copy vs deep copy
		
- java input and output
	- console class
	- readline
	- readpassword
	- generating output
	- println, print, printf
	
	
## week 3

	.  
	.  
	.  
	
























---

# coding bits

- println and print

- public static void main....
	- static public void main(String[] args){ also works

- in terminal : first javac file name. then java file name

comment out
```java
/* com
this is a multiline coment
ments */  

// this is a single line comment
```

- agar result float he to input bhi as float define karna hoga.

- Notice that the System.out.println( ) statement involves the ‘+’ operator. In this context,
‘+’ means “string concatenation” and, if necessary, “string conversion.” When the compiler
sees a String followed by a ‘+’ followed by a non-String, it attempts to convert the non-
String into a String. 

use of class in java
```java
class Stu{
String name;
int age;
double ht;
}

public class Ab {
public static void main(String[] args){
Stu amit = new Stu();
Stu veer = new Stu();
amit.name = "Amit";
amit.age = 32;
amit.ht = 5.10;
veer.name = "Veer";
veer.age = 19;
veer.ht = 6.2;

System.out.println(veer.ht);
}
}

>> 19
```

- addition (+), subtraction (-), division (/), multiplication (*) and modulus (%, which produces the remainder from integer division).

```java
import java.util.*;

public class Ac{
public static void main(String[] args) {
Random ra = new Random(100);
int a, b, c;
a = ra.nextInt(40);
b = ra.nextInt(400); // 400 is upper bound
System.out.println(b);
System.out.println(a + b);
System.out.println(a);
System.out.println(++a);
System.out.println(--a);
System.out.println(--a);
System.out.println(--a);
System.out.println(a);

double x, y, z;
x = ra.nextDouble(5);
System.out.println(x);
System.out.println(++x);
System.out.println(++x);
}
}
```

- AND (&&), OR (||) and NOT (!) 

##### if condition

```java
class Example{
   public static void main(String[] args_) {
      int num;
      num = 500;
      if (num < 100)
         System.out.println("lesser");
   }
}

>> (empty, nothing in output)
```

```java
class Example{
   public static void main(String[] args_) {
      int num;
      num = 500;
      if (num < 100)
         System.out.println("lesser");
   }
}

>> lesser
```

```java
class Example{
   public static void main(String[] args){
      int x, y;
      x = 20;
      y = 20;
      if (x < y){
         System.out.println("X is lesser than Y");
      }
      if (x > y){
         System.out.println("Y is lesser than X.");
      }
      if (x == y){
         System.out.println("they are equal.");
      }
   }
}

>> they are equal.
```
you can use { or not after if statement.

```java
class Example{
   public static void main(String[] args){
      int x, y;
      x = 20;
      y = 20;
      if (x < y){
         System.out.println("X is lesser than Y");
      }
      else
         System.out.println("somehting else but not lesser.");
   }
}

>> somehting else but not lesser.
```

- same for else also you can use  { } or not.

- there is no **elif** in java. you need to use *else if* .

```java
class Example{
   public static void main(String[] args){
   int x = 1000;
   System.out.println("Code start");
   if (x < 10) System.out.println("Small");
   else if (x < 30) System.out.println("mid");
   else System.out.println("huge");
   }}

>> Code start
>> huge
```

**Simplest for loop structure.**
- for(initialization; condition; iteration) statement;
- above sequence is really important.

```java
class Example{
   public static void main(String[] args){
   int x ;
   for(x = 0; x < 10; x = x+1)
   System.out.println(x);
   }}

>> 0 to 9
```

```java
class Example{
   public static void main(String[] args){
   int x ;
   for(x = 0; x = x+1; x < 10)
   System.out.println(x);
   }}

>> error
```

- x++ : increase 1 value
- x-- : decrease 1 value

```java
class Example{
public static void main(String[] args){
int x, y;
y = 20;
for(x = 0; x <= 10; x++){
System.out.println("This is x"+x);
System.out.println("This is y"+y);
y = y - 2;
}}}
```
- above is an example of multiblock code. here we have more than 1 output block.

- while declaring / initializing any variable you need to choose data type very carefully.  If data type is not correct then your code will give wrong answer. 

finding data type in java
```java
class Example{
public static void main(String[] args){
Integer x = 100;
System.out.println(x.getClass().getName());
}}

>> java.lang.Integer
```

```java
class Example{
public static void main(String[] args){
int a = 10, b = 3;
int c = a*3;
System.out.println("value of a and b and c "+a + b + c);
System.out.println(Math.sqrt(a));
}}

>> value of a and b and c 10330
>> 3.1622776601683795
```
- above is an example of Dynamic Initialization.
- and Math library / class (predefine in Java)

```java
class Example{
public static void main(String[] args){
int[] x;
x = new int[4];
x[0] = 10;
x[1] = 123;
x[2] = 34;
x[3] = 26;
System.out.println(x[2]);
System.out.println(x);
}}

>> 34
>> I@24d46ca6  idk some random stuff.
```


