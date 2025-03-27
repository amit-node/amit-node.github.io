---
title: Java self study - Coding
date: 2025-03-27
tags:
  - java
---
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
- char, single quote, shirf character hoga, hamesha
- string, hamesha double quote
- float  ki jagah jyadatar double use karna better hoga. 
- 

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

- addition (+), subtraction (-), division (/), multiplication (\*) and modulus (%, which produces the remainder from integer division).

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

>> 250
>> 285
>> 35
>> 36
>> 35
>> 34
>> 33
>> 33
>> 0.9748802867385259
>> 1.974880286738526
>> 2.974880286738526
```
- yaha ++a, a me ek value badha dega. but a++ kaam nahi karta. 
- AND (&&), OR (||) and NOT (!) 

##### if condition
 structure : " if (condition) statement "
```java
class Example{
   public static void main(String[] args) {
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
   public static void main(String[] args) {
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

- same for else also you can use  { } or not. but use {} all the time. it really prevent errors.

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

##### **Simplest for loop structure.**
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


##### writhing *functions* in java
```java
class ZZZ{
static void myFunction(){
System.out.println("myFunction is executed.");
}

public static void main(String[] args){
myFunction();
}
}

>> myFunction is executed.
```


- in java booleans are "true" and "false". small case. not True and False.

##### Array :
- 1-d array : list of like - typed variables.
- first define a variable as array : data-type [] variable-name
- then define it's size (memory allocation) : variable-name = new type [size]
- then add elements.
- be careful about the data type. 
- we can also change any list element dynamically

```java
class Example{
   public static void main(String[] args){
      String [] name_list;
      name_list = new String[5];
      name_list[0] = "amit";
      name_list[1] = "Mathew";
      name_list[2] = "Sujay";
      name_list[3] = "Veer";
      name_list[4] = "Raj";
      System.out.println(name_list);
      System.out.println(name_list[1]);
      System.out.println(name_list[3]);
      name_list[1] = "Abhijeet";
      System.out.println(name_list[1]);
   }
}

>> [Ljava.lang.String;@24d46ca6
>> Mathew
>> Veer
>> Abhijeet
```

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

##### User input
- import Scanner class in java.util to get user input. java.util inbuilt library he. 
- make a placeholder of type scanner, call new scanner with System.in.
- initialize and define our variable and read placeholder.
- 

```java
import java.util.*;

class Example{
public static void main(String[] args){
Scanner tumharaVariable = new Scanner(System.in);
String tumharaVariable_2 = tumharaVariable.nextLine();

System.out.println(tumharaVariable_2);
}}

>> input : HTIC
>> HTIC
```


>Write a Java program that asks the user to enter **5 numbers** (integers).
>- The program should count how many numbers are **even** and how many are **odd**.
>- After all numbers are entered, print the count of **even** and **odd** numbers.

```java
import java.util.*;

class Example{
public static void main(String[] args){
int x;
Scanner obj = new Scanner(System.in);

for (x = 0; x < 5; x++) {
   System.out.println("input de int :");
   int num = obj.nextInt();
   if (num % 2 == 0) System.out.println(num +" Even ");
   else System.out.println(num + " Odd ");
   }
}}
```

##### Constructor
A constructor in Java is a special method that is used to initialize objects when they are created. It has the same name as the class and does not have a return type (not even void).

# Study for OPPE 2

### Week 2 ppa 1
ht and wd is given. find area of the rectangle
```java
class Rectangle{
public static void main(String[] args){
int w = 10;
int h = 20;
int area = w * h;
System.out.println(area);
}
}

>> 200
```

Now ask w and h as input.
```java
import java.util.*;                             //new line

class Rectangle{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);                   //new line
int w = Integer.parseInt(sc.nextLine());        // changed line
int h = Integer.parseInt(sc.nextLine());          // changed line
int area = w*h;
System.out.println(area);
}
}
```

Now make  a function, which initiate height and width and return area.  
And a piece of code which ask for input and return area.  
```java
import java.util.*;

class RecFunc{
int w, h;
public void setw(int w_input){             // setw is a function
w = w_input; }
public void seth(int h_input){             // seth is a function
h = h_input; }
public int area(){                    // area is a functiomn
return w*h; }
}                              // don't forget to close RecFun class

public class Rectangle{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int w_input = Integer.parseInt(sc.nextLine());
int h_input = Integer.parseInt(sc.nextLine());
int area_of_rectangle;

RecFunc r = new RecFunc();            // calling new class is necessary
r.setw(w_input);
r.seth(h_input);
area_of_rectangle = r.area();
System.out.println(area_of_rectangle);
}}
```

