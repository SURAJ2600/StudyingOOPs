# **Object Oriented Programming in Java**
[Source](https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/ "Visit Geek for geeks!")

Object Oriented Programming aims to implement real world entities 
like Inheritance, Polymorphism, Encapsulation in programming. 

The main aim is to bind together the data and the functions 
so that other parts of the code cannot access them.  

>### **OOPs Concepts**
+ [Polymorphism](#polymorphism)
    + [Overloading](#overloading)
    + [Overriding](#overriding)
+ Inheritance
+ Encapsulation
+ Abstraction
+ Class
+ Object
+ Method
+ Message Passing

# **Polymorphism**

The word polymorphism means having many forms. In simple words, 
we can define polymorphism as the ability of a message to be 
displayed in more than one form.
 
**Real Life Example:** A Person at the same time can have different 
characteristics. A man can be a father, a brother, a son, a friend 
in different situations.

Polymorphism is the ability of OOPs programming languages to differentiate
between entities of the same name. Its done in Java with the help of 
signature and declaration of the entities 

Polymorphism is of 2 types:  
1. Overloading 
1. Overriding 

## **Overloading** 

([source](https://www.geeksforgeeks.org/overloading-in-java/))

Overloading allows methods to have same name but different signatures
where the signature can differ by methods having different types of input
parameters or different number of input parameters.

[Example](https://github.com/debajyotibasak/StudyingOOPs/blob/master/src/com/debo/java/oops/polymorphism/overloading/Sum.java)

>### **Types of Overloading**
+ [Changing type of parameters](https://github.com/debajyotibasak/StudyingOOPs/blob/master/src/com/debo/java/oops/polymorphism/overloading/TypeChange.java)
+ [Changing number of parameters](https://github.com/debajyotibasak/StudyingOOPs/blob/master/src/com/debo/java/oops/polymorphism/overloading/NumberChange.java)
+ [Changing order of parameters](https://github.com/debajyotibasak/StudyingOOPs/blob/master/src/com/debo/java/oops/polymorphism/overloading/OrderChange.java)

**What if the prototype does not match with arguments?**

Priority wise, compiler take these steps:
1. Type Conversion but to higher type (in terms of range) in same family.
1. Type conversion to next higher family (suppose if there 
is no long data type available for an int data type, 
then it will search for float data type).

[Example](https://github.com/debajyotibasak/StudyingOOPs/blob/master/src/com/debo/java/oops/polymorphism/overloading/Display.java)

**Advantage**

We don't have to create redundant method names for similar kind of tasks.

**Can we overload static methods?**

Yes. We can have two ore more static methods with same name, 
but differences in input parameters. 

**Can we overload methods that differ only by static keyword?**

We cannot overload two methods in Java if they differ only 
by static keyword. ([Source](https://www.geeksforgeeks.org/can-we-overload-or-override-static-methods-in-java/))

**Can we overload main() in Java?**

Like other static methods, we can overload main() in Java.

**What is the difference between Overloading and Overriding?**
+ Overloading is about same function have different signatures. 
Overriding is about same function, same signature but different 
classes connected through inheritance.
+ Overloading is an example of compiler time polymorphism and 
overriding is an example of run time polymorphism.

<br></br>
![Overloading vs Overriding](https://media.geeksforgeeks.org/wp-content/uploads/OverridingVsOverloading.png)
<br></br>

[Method overloading and null error in Java](https://www.geeksforgeeks.org/method-overloading-null-error-java/)
<br></br>

## **Overriding** 

In Object oriented programming, overriding is a feature that 
allows a subclass or a child class to provide a specific 
implementation of a method which already provided by its parent
class or super class.

The method in the subclass is said to **Override** the method in 
the superclass

The version of a method that is executed will be determined 
by the object that is used to invoke it. 

If an object of a parent class is used to invoke the method, 
then the version in the parent class will be executed, 
but if an object of the subclass is used to invoke the method, 
then the version in the child class will be executed.

In other words, it is the type of the object being referred 
to (not the type of the reference variable) that determines 
which version of an overridden method will be executed.

[Example](https://github.com/debajyotibasak/StudyingOOPs/blob/master/src/com/debo/java/oops/polymorphism/overriding/Example1.java)

>### **Rules for Overriding**
1. [Overriding and access modifiers.](#overriding-and-access-modifiers)
1. [Final methods cannot be overridden.](#final-methods-cannot-be-overridden)
1. [Static methods cannot be overridden.](#static-methods-cannot-be-overridden)
1. Private methods cannot be overridden.
1. The overriding method must return the same subtype.
1. Invoking overridden methods from subclass.
1. Overriding and constructor.
1. Overriding and Exception-Handling.
    1. Rule 1.
    1. Rule 2.
1. Overriding and abstract method.
1. Overriding and synchronized/strictfp method. 

### **Overriding and access modifiers** 
The access modifier for an overriding method can allow more access than
its overridden method but not less access.

For example: A method with Protected instance can be provided with a 
public access modifier but not private

[Example](https://github.com/debajyotibasak/StudyingOOPs/blob/master/src/com/debo/java/oops/polymorphism/overriding/Access.java) 

### **Final methods cannot be overridden** 
If we do not want a method to be overridden, we declare it as a final.

[Example](https://github.com/debajyotibasak/StudyingOOPs/blob/master/src/com/debo/java/oops/polymorphism/overriding/FinalNotOverridden.java)

### **Static methods cannot be overridden**
Static methods of the base class cannot be overridden by the child class.

So when we define a static method with the same signature as in the 
base class it is called **Method hiding**.

[Example](https://github.com/debajyotibasak/StudyingOOPs/blob/master/src/com/debo/java/oops/polymorphism/overriding/StaticNotOverridden.java)