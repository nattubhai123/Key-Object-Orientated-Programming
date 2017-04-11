# Key-Object-Orientated-Programming
Key Object Orientated Programming (OOP)



1.	Encapsulation: 
Encapsulation is one of the important features of OOP, basically it’s a process of bindind or wrapping the data and codes that operates on the data in to a single entity. This keeps the data safe from outside interface and misuse. In other word, it’s a protective wrapper that prevents code and data from being arbitrarily accessed by other code defined outside the wrapper.

Why need encapsulation?
•	Combining data and how it’s manipulated in one place: This is achieved through the state (the private field) and the behaviors (the public methods) of an object.
•	Only allowing the state of an object to be accessed and modified through behaviors: The values contained with in an object’s state can then be strictly controlled.
•	Hiding the details of how the object works: The only part of the object that is accessible to the outside world is its behaviors. What happens inside those behaviors and how the state is stored is hidden from view.
•	Benefits: The main benefit of encapsulation is the ability to modify the implemented code without breaking the code of others who use the implemented code. 
Example:

Class Employee
{
private String name;

public String getName()
{
return name;
}
public void setName(String name){
this.name=name:
}
{

class Demo
{
public static void main(String[] args)
{
Employee e=new Employee();
e.setName(“Raj”);
System.out.println(e.getName());
}
{

2.	Inheritance:
Inheritance is a relation between two or more classes where derived class inherits behaviour and attributes of pre-existing (base) classes. Intended to help reuse of existing code with little or no modification. The existing class is called the base class and the new class is called the derived class, other programming language such as Java and C#, refer to the base class as the superclass and the derived class as the subclass. A derived class represents a more specialized group of objects.

Example:
Class sum        //Super class
{
int a=10;
int b=20;
void show1()
{
System.out.println(“value of a :- “+a);
System.out.println(“value of b :- “+b);
}
         }
          class sum2 extends sum        //base class
         {
            public static void main(String args[])
            {
                      sum2obj =new sum2();
                       obj.show1 ();
           }
           {




3.	Polymorphism:
Polymorphism in Java program refers to the ability of a reference variable to change behavior according to what object instance it is holding.
This allows multiple oblects of different subclasses to be treated as objects of a single super class, while automatically selecting the proper methods to apply to a particular object based on the subclass it belongs to for example, given a base class shape, polymorphism enables the programmer to define different area methods for any number of derived classes. No matter what shape an object is, applying the area method to it will return the correct result.

Example:
Public static main ( String [] args )  {
  Student studentObject = new Student ();
  Employee employeeObject = new Employee ();

Person ref = studentObject;  // Person reference points 
                                              // to a Student object
// Calling getName () of the Student object instance
String name = ref.getName ();
}

public class student   {
     public String getName () {
        System.out.println (“Student Name :” = name );
         Return name;
   }
}

public class Employee   {
     public String getName() {
           System.out.println (“Employee Name:” + name);
            Return name;
      }
}



4.	Abstraction:
Abstraction is the concept of exposing only the required essential characteristics and behavior with respect to a context. Hiding of data is known as data abstraction. In object, oriented programming language this is implemented automatically while writing the code in the form of class and object. A class which contains the abstract keyword in its declaration is known as abstract class.
Abstract classes may or may not contain abstract methods, i.e., methods without body (public void get () ;)
But, if a class has at least one abstract method, then the class must be declared abstract. If a class is declared abstract, it cannot be instantiated. To use an abstract class, you should inherit it from another class, provide implementations to the abstract methods in it. If you inherit an abstract class, you should provide implementations to all the abstract methods in it.
Example:
abstract class Bank {    
abstract int getRateOfInterest();    
}    
class X extends Bank{    
int getRateOfInterest(){return ;}    
}    
class Y extends Bank{    
int getRateOfInterest(){return ;}    
}    
    
class TestBank{    
public static void main(String args[]){    
Bank b;  
b=new X();  
System.out.println("Rate of Interest is: "+b.getRateOfInterest()+" %");    
b=new Y ();  
System.out.println("Rate of Interest is: "+b.getRateOfInterest()+" %");    
}}    
