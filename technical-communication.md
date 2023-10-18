# **Major Concepts of OOPS**

 OOPs stands for Object Oriented Programming and is used in many languages like Java, C++, C#, Ruby, etc. It helps in building complex architecture using reusable and simple code. It allows programmers to make changes in code base without altering entire system.

OOPs is mainly based on **Class** and **Objects**. Class in templete or a blueprint consisting of all the properties and methods.
When an instance of that class is created or as we call the Object of that class is created, some memory is allocated to that object. 
*(In this report I will use Java to explain the OOPs Concepts)*

Ex:-
```
public class Bike {
 int maxSpeed;
 String color;
 int mileage;
 // This method will print out the value of maxSpeed variable.
 public int getMaxSpeed(){
  System.out.println(maxSpeed);
  }
} 
```
---
Major concepts of OOPs include **Inheritance, Polymorphism, Abstraction and Encapsulation.**

### **1. Inheritance**

In OOPs if there is class which has all the properties and methods which we want in our class and build a new class which has some extra data members and methods then we can use Inheritance in that case.
   Basically we can use extend keyword in Java to inherit all the properties of Parent class.
   
  Ex:- 
```
class Parent {
 int number = 10;
 public void parentMethod(){
  System.out.println("Using method of parent class");
  }
}

class Child extends Parent{
// parent class method used in child class
parentMethod();
// parent class variable used in child class method
 public void childMethod(){
  System.out.println("Using parent class attribute"+ number); 
  }
}
```
### **2. Polymorphism**

Suppose there is a method in a class and we want to change functionality of that method. In that case we will need to change that methods body according to our needs. By doing this we are morphing the
original method. We can do that in java in different ways like Overloading and Overriding a method.

Example:
```
class Parent {
//two arguments passed for product of two numbers
 public void productOfNumbers(int a, int b){
  System.out.println("Product of two numbers is:-" + a*b);
  }
//three arguments passed for product of three numbers
public void productOfNumbers(int a, int b, int c){
  System.out.println("Product of three numbers is:-" + a*b*c);
  }
//four arguments passed for product of four numbers
public void productOfNumbers(int a, int b, int c, int d){
  System.out.println("Product of four numbers is:-" + a*b*c*d);
  }
 }
```

### **3. Abstraction**

In OOPs if we want to hide the implimentation details and just give the funtionality to the user then we can do that by Abstraction.
Here we just define the methods giving a general idea of what it does. Then it is upto user about he goes about to add the body of that method. There are two main concepts in Java to achieve that, Abstract classes and Interfaces. 
* Abstract classes contains abstract methods and non-abstract methods.
* Interfaces only contains abstract methods.

Example:
```
//Abstract class
abstract class Parent {
 abstract public void parentMethod();
}
class Child extends Parent{
@Override
 public void parentMethod(){
  System.out.println("Print using abstract parent method");; 
 }
}
// Interface
interface firstInterface{
 abstract public void firstInterfaceMethod();
}
interface secondInterface{
 abstract public void secondInterfaceMethod();
}
//Multiple interfaces implemented in a single class
class Child implements firstInterface, secondInterface{
@Override
 public void firstInterfaceMethod(){
  System.out.println("Print using abstract method from of interface");; 
 }
@Override
 public void secondInterfaceMethod(){
  System.out.println("Print using abstract method of second interface");; 
 }
}
```

### **4. Encapsulation**

If we want to protect some data from certain members then we will need to build a barrier on who can access what kind of data and ultimatly change it. For that in Java we have different access modifiers like Public, Default, Protected and Private.

* In Private we can share the data within a class.
* In Default data can be shared within package.
* In Protected data can be shared inside the package and with subclasses.
* In Public data can be shared anywhere within class, package or subclasses.
 
 Example:
 ```
 public class Student{  
//private data member  
private String name;  
//getter method for name  
public String getName(){  
return name;  
}  
//setter method for name  
public void setName(String name){  
this.name=name  
}  
}  
class Test{  
public static void main(String[] args){  
//creating instance of the encapsulated class  
Student s=new Student();  
//setting value in the name member  
s.setName("vijay");  
//getting value of the name member  
System.out.println(s.getName());  
}  
}
```

Here, by using private on our variables and getters and setter methods for those variables we can choose how to share the variables and change those variables.
 
### Conclusion

Use of OOPs concepts helps programmer tackle complex functionality in a structured way and therefore recommended to learn it. This blog just scraches the surface of OOPs and we can do much more with it.

Links:-
1. [(https://www.javatpoint.com/java-oops-concepts)] 
2. [(https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/)]
