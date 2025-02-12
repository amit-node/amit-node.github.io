---
title: Java self study
date: 2025-02-12
tags:
  - BS_degree
  - Study
---
# Preface
- It is still the first and best choice for developing web-based applications.
- This book following Java SE (JDK 17)
- This book is divided into 4 parts
	- Part I presents an in-depth tutorial of the Java language.
	- Part II examines key aspects of Java’s standard API library.
	- Part III offers three chapters that introduce Swing.
	- Part IV contains two chapters that show examples of Java in action.
---
{{< br >}}

# Ch 1. The History and Evolution of Java
- Many features of Java are influenced by C and C++
- Invented and first implemented by Dennis Ritchie on a DEC PDP-11 running the UNIX operating system, C was the result of a development process that started with an older language called BCPL, developed by Martin Richards. BCPL influenced a language called B, invented by Ken Thompson, which led to the development of C in the 1970s.
- C++ was invented by Bjarne Stroustrup in 1979, while he was working at Bell Laboratories in Murray Hill, New Jersey. Stroustrup initially called the new language “C with Classes.” However, in 1983, the name was changed to C++. C++ extends C by adding object-oriented features. Because C++ is built on the foundation of C, it includes all of C’s features, attributes and benefits
- Java was conceived by James Gosling, Patrick Naughton, Chris Warth, Ed Frank, and Mike Sheridan at Sun Microsystems, Inc. in 1991. It took 18 months to develop the first working version. This language was initially called “Oak,” but was renamed “Java” in 1995.
- Computer languages evolve for two reasons: to adapt to changes in environment and to implement advances in the art of programming.
{{< br >}}
{{< br >}}

JVM : Java Virtual Machine  
JRE : Java Runtime Environment  
The output of a Java compiler is not executable code. Rather, it is bytecode. Bytecode is a highly optimized set of instructions designed to be executed by what is called the Java Virtual Machine (JVM), which is part of the Java Runtime Environment (JRE). In essence, the original JVM was designed as an interpreter for bytecode.

> our code > compile > bytecode > run > result


### 12 main characteristics of Java
1. **Simple** : Simple to learn, based on C++
2. **Object Oriented** : Everything in java is an object. In object oriented programming, we organize our software as a combination of different types of objects.
3. **Platform independent** : You can use Java on any platform : mac, Windows, Linux.
   -  There are two type of platforms : hardware based and software based. Java works on software based platform.
4. **Secured** : java programs run inside a virtual machine sandbox.
5. **Robust** : Strong memory management.  
			Java is a strictly typed language, it checks your code at compile time. 
1. **Architectural - Neutral** : No implementation dependent features.
2. **Portable** : You can carry Java bytecode to any platform.
3. **High Performance** : java is faster than many languages. But slower than C++. because Java is an interpreted language, which are slower than compiled languages (C++).
   1. A **compiler** translates the entire source code into machine code than executes it. Results in faster execution.
   2. **Interpreter** translate code line by line during execution. making it easier to detect errors but slows down program.
4. **Interpreted**
5. **Distributed** : It facilitates users to create distributed applications in Java.
6. **Multi-threaded** : Java can deal with many tasks at once by defining multiple threads.  
			Java also supports Remote Method Invocation (RMI). This feature enables a program to invoke methods across a network.
7. **Dynamic** : It supports dynamic loading of classes
---
{{< br >}}
# Ch 2. An Overview of Java
Object-oriented programming (OOP) is at the core of Java. In fact, all Java programs are to at least some extent object-oriented. OOP is so integral to Java that it is best to understand its basic principles before you begin writing even simple Java programs.

### Two Paradigms
 Some programs are written around “what is happening” (process oriented model) and others are written around “who is being affected” (object oriented programming) These are the two paradigms that govern how a program is constructed. 

### Abstraction
An essential element of object-oriented programming is abstraction. Humans manage complexity through abstraction. For example, people do not think of a car as a set of tens of thousands of individual parts. They think of it as a well-defined object with its own unique behavior. This abstraction allows people to use a car to drive to the grocery store without being overwhelmed by the complexity of the individual parts. They can ignore the details of how the engine, transmission, and braking systems work. Instead, they are free to utilize the object as a whole.

### The Three OOP Principles
#### a. Encapsulation

#### b. Inheritance
#### c. Polymorphism







---
**Notes**
Stack memory is a memory usage mechanism that allows the system memory to be used as temporary data storage that behaves as a first-in-last-out buffer.

---
println and print

public static void main....
static public void main(String[] args){ also works

in terminal : first javac file name. then java file name

```java
/* com
this is a multiline coment
ments */  

// this is a single line comment
```

agar result float he to input bhi as float define karna hoga.

Notice that the System.out.println( ) statement involves the ‘+’ operator. In this context,
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
```
> 19

addition (+), subtraction (-), division (/), multiplication (*) and modulus (%,
which produces the remainder from integer division).

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

AND (&&), OR (||) and NOT (!) 

