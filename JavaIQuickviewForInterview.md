
#### JAVA QUICKVIEW INTERVIEWS AND ANSWER 
### OOPS
OOPS is a methodology or paradigm to design a program using classes and objects. It simplifies the software development and maintenance by providing some concepts:

#### Object 
Any entity that has state and behavior is known as an object. For example: chair, pen, table, keyboard, bike etc. It can be physical and logical.
#### Class
Collection of objects is called class. It is a logical entity.

### Data Hiding: 
- Our internal data should not go out directly that is outside person can’t access our internal data directly.
- By using private modifier we can implement data hiding.adv of data hiding is security.
- Note: recommended modifier for data members is private.

### Abstraction: 
	Hide internal implementation and just highlight the set of services,is called abstraction.
-  By using abstract classes and interfaces we can implement abstraction.
 - Abstraction is more about ‘What‘a class can do.
 - Encapsulation is more about ‘How‘to achieve that functionality.

### Encapsulation: (singalton dp)
It is the process of Encapsulating data and corresponding methods into a single module. Encapsulation is a process of wrapping of data and methods in a single unit is called encapsulation. Encapsulation is achieved in java language by class concept.
- If any java class follows data hiding and abstraction such type of class is said to be encapsulated class.   
         ```Encapsulation=Datahiding+Abstraction ```

###### What is the difference b/w abstraction and encapsulation while they both are hiding the implementation from user.
“Abstraction is implemented using interface and abstract class while Encapsulation is implemented using private and protected access modifier.”
###### How to implement encapsulation in java:
1) Make the instance variables private so that they cannot be accessed directly from outside the class. You can only set and get values of these variables through the methods of the class.
2) Have getter and setter methods in the class to set and get the values of the fields
###### Example:
- 	In encapsulated class we have to maintain getter and setter methods for every data member.
- The main disadvantage of encapsulation is it increases length of the code and slows down execution.
To achieve encapsulation in Java: Declare the variables of a class as private.
Provide public setter and getter methods to modify and view the variables values. The Java Bean class is the example of fully encapsulated class.

### Polymorphism: (Adapter Dp):
Same name with different forms is the concept of polymorphism.Polymorphism is the ability of an object to take on many forms.The most common use of polymorphism in OOP occurs when a parent class reference is used to refer to a child class object.

###### Example 1:
We can use same abs() method for int type, long type, float type etc.
abs(int)   abs(long)    abs(float)
###### Example 2: 
We can use the same List reference to hold ArrayList object, LinkedList object, Vector object, or Stack object.
###### Example:
1)	List l=new ArrayList();2)List l=new LinkedList();3)List l=new Vector();
4) List l=new Stack();

The best exp  of polymorphism is, in our project we have implemented, build the response.If it is success we are calling one method buildResponse(obj.). If it is failure we will call same buildResponse(String respCode, String respMsg). But method parameter must be different.

 
1)	Inheritance talks about reusability.
2)  Polymorphism talks about flexibility.
3)	Encapsulation talks about security.
### IS-A Relationship(inheritance):
1) Also known as inheritance.
2) By using extends keywords we can implement IS-A relationship.
3) The main advantage of IS-A relationship is reusability.
=>To reduce the complexity and simplify the language, multiple inheritance is not supported in java.Consider a scenario where A, B and C are three classes. The C class inherits A and B classes. If A and B classes have same method and you call it from child class object, there will be ambiguity to call method of A or B class.
Since compile time errors are better than runtime errors, java renders compile time error if you inherit 2 classes. So whether you have same method or different, there will be compile time error now.
```
 class Employee{  
 float salary=40000;  }  
class Programmer extends Employee{  
 int bonus=10000;  
 public static void main(String args[]){  
   Programmer p=new Programmer();  
   System.out.println("Programmer salary is:"+p.salary);  
   System.out.println("Bonus of Programmer is:"+p.bonus);  
}
} 
```
### HAS-A relationship:
1)	HAS-A relationship is also known as composition (or) aggregation.
2)	There is no specific keyword to implement hAS-A relationship but mostly we can use new operator.
3)	The main advantage of HAS-A relationship is reusability.
Example:
```
     class Engine {
	//engine specific functionality
}
class Car{
	Engine e=new Engine();
	//........................;
}
```
•	Class Car HAS-A engine reference.
•	HAS-A relationship increases dependency between the components and creates maintains problems.
### Composition vs Aggregation:
### Composition:
- Without existing container object if there is no chance of existing contained objects then the relationship between container object and contained object is called composition which is a strong association.
###### Example:
•	University consists of several departments whenever university object destroys automatically all the department objects will be destroyed that is without existing university object there is no chance of existing dependent object hence these are strongly associated and this relationship is called composition.
### Aggregation:
- Without existing container object if there is a chance of existing contained objects such type of relationship is called aggregation. In aggregation objects have weak association.
###### Example:
•	Within a department there may be a chance of several professors will work whenever we are closing department still there may be a chance of  existing professor object without existing department object the relationship between department and professor is called aggregation where the objects having weak association.
Method signature: In java method signature consists of name of the method followed by argument types.In java return type is not part of the method signature.

### Overloading:
•	Two methods are said to be overload if and only if both having the same name but different argument types.
•	But in java we can take multiple methods with the same name and difft argument types.
•	Having the same name and different argument types is called method overloading.
•	All these methods are considered as overloaded methods.
•	Having overloading concept in java reduces complexity of the programming.
•	Method overloading is performed within class.
###### Three(3) ways to overload a method:
In order to overload a method, the argument lists of the methods must differ in either of these

1. Number of parameters:For Exp: valid case of overloading    add(int, int),add(int, int, int)
2. Data type of parameters:For example:add(int, int),add(int, float)
3. Sequence of Data type of parameters:For example:add(int, float),add(float, int)

###### Valid/invalid cases of method overloading
Case 1:  int mymethod(int a, int b, float c),int mymethod(int var1, int var2, float var3)
Result: Compile time error. Argument lists are exactly same. Both methods are having same number, data types and same sequence of data types.

Case 2: int mymethod(int a, int b),int mymethod(float var1, float var2)
Result: Perfectly fine. Valid case of overloading. Here data types of arguments are different.

Case 3: int mymethod(int a, int b),int mymethod(int num)
Result: Perfectly fine. Valid case of overloading. Here number of arguments are different.

Case 4: float mymethod(int a, float b),float mymethod(float var1, int var2)
Result: Perfectly fine. Valid case of overloading. Sequence of the data types of parameters are different, first method is having (int, float) and second is having (float, int).

Case 5: int mymethod(int a, int b),float mymethod(int var1, int var2)
Result: Compile time error. Argument lists are exactly same. Even though return type of methods are different, it is not a valid case. Since return type of method doesn’t matter while overloading a method.

1 – return type, method name and argument list same. 2 – return type is different. Method name & argument list same---compilation error
- method overloading can't be performed by changing return type of the method only. Return type can be same or different in method overloading. But you must have to change the parameter.
```
class OverloadingExample{  
static int add(int a,int b){return a+b;}  
static int add(int a,int b,int c){return a+b+c;}  
}  
And  
static int add(int a,int b){return a+b;}  
static double add(int a,int b){return a+b;}  
              Compile Time Error: method add(int,int) is already defined in class Adder.
```
###### Tips:
Yes, by method overloading. You can have any number of main methods in a class by methodoverloading. But JVM calls main() method which receives string array as arguments only.


•	In overloading compiler is responsible to perform method resolution(decision) based on the reference type. Hence overloading is also considered as compile time polymorphism(or) static ()early biding.

            Automatic promotion in overloading. 
•	In OL if compiler is unable to find the method with exact match we won’t get any compile time error immediately.
•	The following are various possible automatic promotions in overloading.
•	In overloading Child will always get high priority then Parent.
•	In general var-arg method will get less priority that is if no other method matched then only var-arg method will get chance for execution it is almost same as default case inside switch.
•	In overloading method resolution is always based on reference type and runtime object won’t play any role in overloading.
```
byte → short → int → long
short → int → long
int → long → float → double
float → double
long → float → double
```
### Overriding:
•	Whatever the Parent has by default available to the Child through inheritance, if the Child is   not satisfied with Parent class method impln then Child is allow to redefine that Parent class method in Child class in its own way this process is called overriding. OR
•	If subclass (child class) has the same method as declared in the parent class, it is known as method overriding in Java.
•	In other words, If a subclass provides the specific implementation of the method that has been declared by one of its parent class, it is known as method overriding.
•	The Parent class method which is overridden is called overridden method.
•	The Child class method which is overriding is called overriding method.
###### Note: In overriding runtime object will play the role and reference type is dummy.
### Rules for overriding:
•	In overriding method names and arguments must be same. That is method signature must be same.
•	Until 1.4 version the return types must be same but from 1.5 version onwards co-variant return types are allowed.
•	According to this Child class method return type need not be same as Parent class method return type its Child types also allowed.
•	Method overriding occurs in two classes that have IS-A (inheritance) relationship.
•	Method overriding is used to provide the specific implementation of the method that is already provided by its super class.
•	It is valid in “1.5” but invalid in “1.4”.
•	Co-variant return type concept is applicable only for object types but not for primitives.
•	Private methods are not visible in the Child classes hence overriding concept is not applicable for private methods. Based on own requirement we can declare the same Parent class private method in child class also. It is valid but not overriding.
###### Example:
•	Parent class non final methods we can override as final in child class. We can override native methods in the child classes.
•	We should override Parent class abstract methods in Child classes to provide impl.
It is valid. It seems to be overriding concept is applicable for static methods but it is not overriding it is met1hod hiding.
 
###### No, Static methods can't be overriden as it is part of a class rather than an object. But one can overload static method. No, you cannot override a static method. The static resolves against the class, not the instance.

•	In overriding method resolution is always takes care by JVM based on runtime object hence overriding is also considered as runtime polymorphism or dynamic polymorphism or late binding.
•	The process of overriding method resolution is also known as dynamic method dispatch. 

1. Overriding refers to the ability of a subclass to re-implement an instance method inherited from a superclass. 
2.    What methods can be overridden ? Rule #1: Only inherited methods can be overridden.
3.   What methods that cannot be overridden?Rule #2: Final and static methods cannot be overridden.
4.    Requirements for the overriding method
With respect to the overridden method, the overriding method must obey the following rules:
Rule #3: The overriding method must have same argument list.
Rule #4: The overriding method must have same return type (or subtype).
Suppose that a Food class has a subclass called DogFood, the following example shows a correct overriding:
Rule #5: The overriding method must not have more restrictive access modifier.
In other words, the overriding(child class) method may have less restrictive (more relaxed) access modifier. The following example shows a legal overriding:
###### 	If the overridden method is has default access, then the overriding one must be default, protected or public.
###### 	If the overridden method is protected, then the overriding one must be protected or public.
###### 	If the overridden method is public, then the overriding one must be only public.

####  Access modifier restrictions in decreasing order:
•	private
•	default
•	protected
•	public

https://www.codejava.net/java-core/the-java-language/12-rules-of-overriding-in-java-you-should-know

Rule #6: The overriding method must not throw new or broader checked exceptions.
In other words, the overriding method may throw fewer or narrower checked exceptions, or any unchecked exceptions. 
5.    Invoking the overridden method
Rule #7: Use the super keyword to invoke the overridden method from a subclass.
6.    Overriding and constructor
Rule #8: Constructors cannot be overridden.
7.    Overriding and abstract method
Rule #9: Abstract methods must be overridden by the first concrete (non-abstract) subclass.
8.    Overriding and static method
Rule #10: A static method in a subclass may hide another static one in a superclass, and that’s called hiding.
9.    Overriding and synchronized method
Rule #11: The synchronized modifier has no effect on the rules of overriding.
10.    Overriding and strictfp method
Rule #12: The strictfp modifier has no effect on the rules of overriding.
That means the presence or absence of the strictfp modifier has absolutely no effect on the rules of overriding: it’s possible that a FP-strict method can override a non-FP-strict one and vice-versa.
### METHOD HIDING
- All rules of method hiding are exactly same as overriding except the following differences.

|Overriding|  Method hiding  |
| ------------- | ------------- |
|1. Both Parent and Child class methods should be non static.|	1. Both Parent and Child class methods should be static.|
|2. Method resolution is always takes care by JVM based on runtime object.|	2. Method resolution is always takes care by compiler based on reference type.|
|3. Overriding is also considered as runtime polymorphism (or) dynamic polymorphism (or) late binding.|	3. Method hiding is also considered as compile time polymorphism (or) static polymorphism (or) early biding.|

### Overloading and method Overriding Differences in java

|NO |Method Overloading |Method Overriding |
| -----|---------- |----------|
|1)|	MO is used to increase the readability of the program.|	MO is used to provide the specific implementation of the methodthat is already provided by its super class.|
|2)|	MO is performed within class.|	MO occurs in two classes that have IS-A (inheritance) relationship.|
|3)|	In case of method overloading, parameter must be different.|	In case of method overriding, parameter must be same.|
|4)|	MO  is exp of compile time polymorphism.	|Method overriding is the example of run time polymorphism.|
|5)|	In java, mo can't be performed by changing return type of the method only. Return type can be same or different in method overloading.| But you must have to change the parameter.	Return type must be same or covariant in method overriding.|

### Differences between overloading and overriding
|Property|	Overloading|	Overriding|
| ------------- | ------------- |-------|
|1)	Method names|	1)	Must be same.| 	1)	Must be same.|
|2)	Argument  type|	2)	Must be different(at least order)|	2)	Must be same including order.|
|3)	Method signature|	3)	Must be different.|	3)	Must be same.|
|4)	Return types	|4)	No restrictions.|	4)	Must be same until 1.4v but from 1.5v onwards we can take co-variant return types also.|
|5)	private,static,final methods|	5)	Can be overloaded.|	5)	Can not be overridden|.
|6)	Access modifiers|	6)	No restrictions.|	6)	Weakering/reducing is not allowed.|
|7)	Throws clause	|7)	No restrictions.|	7)	If child class method throws any checked| exception compulsory parent class method should throw the same checked exceptions or its parent but no restrictions for un-checked exceptions.|
|8)	Method resolution|	8)	Is always takes care by compiler based on referenced type.|	8)	Is always takes care by JVM based on runtime object.|
|9)	Also known as	|9)	Compile time polymorphism (or) static(or)early binding.|	9)	Runtime polymorphism (or) dynamic (or) late binding.?
###### Note: 
In overloading we have to check only method names (must be same) and arguments (must be different) the remaining things like return type extra not required to check.
But In overriding we should compulsory check everything like method names, arguments, return types, throws keyword, modifiers
### Constructors
•	Object creation is not enough compulsory we should perform initialization then only the object is in a position to provide the response properly.
•	Whenever we are creating an object some piece of the code will be executed automatically to perform initialization of an object this piece of the code is nothing but constructor.Hence the main objective of constructor is to perform initialization of an object.
### Constructor Vs instance block:
•	Both instance block and constructor will be executed automatically for every object creation but instance block 1st followed by constructor.
•	The main objective of constructor is to perform initialization of an object.
•	Other than initialization if we want to perform any activity for every object creation we have to define that activity inside instance block.
•	Both concepts having different purposes hence replacing one concept with another concept is not possible.
•	Constructor can take arguments but instance block can’t take any arguments hence we can’t replace constructor concept with instance block.
•	Similarly we can’t replace instance block purpose with constructor.

Static blocks will be executed at the time of class loading hence if we want to perform any activity at the time of class loading we have to define that activity inside static block.

•  With  in  a  class  we  can  take  any  no.  Of  static  blocks  and  all  these  static  blocks  will  be executed from top to bottom.
Static Control Flow is one time activity and it will be executed at the time of class loading. But  instance  control  flow  is  not  one  time  activity  for  every  object  creation  it  will  be executed.
Instance Initializer block is used to initialize the instance data member. It run each time when object of the class is created.
The initialization of the instance variable can be done directly but there can be performed extra operations while initializing the instance variable in the instance initializer block
###### What is invoked first, instance initializer block or constructor?
```
	class Bike8{  
	    int speed;  	      
	    Bike8(){System.out.println("constructor is invoked");}  	   
               	    {System.out.println("instance initializer block invoked");}  
	    public static void main(String args[]){  
	    Bike8 b1=new Bike8();  
	    Bike8 b2=new Bike8();  
	    }      	}  
Output:instance initializer block invoked
       constructor is invoked
       instance initializer block invoked
       constructor is invoked
In the above exp, it seems that instance initializer block is firstly invoked but NO. Instance intializer block is invoked at the time of object creation. The java compiler copies the instance initializer block in the constructor after the first statement super(). So firstly, constructor is invoked. Let's understand it by the figure given below:
Note: The java compiler copies the code of instance initializer block in every constructor.

Rules for instance initializer block :3 rules for the instance initializer block. 
1.	The instance initializer block is created when instance of the class is created.
2.	The instance initializer block is invoked after the parent class constructor is      invoked (i.e. after super() constructor call).
3.	The instance initializer block comes in the order in which they appear.
Program of instance initializer block that is invoked after super()
1.	class A{  
2.	A(){  
3.	System.out.println("parent class constructor invoked");  
4.	}  
5.	}  
6.	class B2 extends A{  
7.	B2(){  
8.	super();  
9.	System.out.println("child class constructor invoked");  
10.	}  
11.	  
12.	{System.out.println("instance initializer block is invoked");}  
13.	  
14.	public static void main(String args[]){  
15.	B2 b=new B2();  
16.	}  
17.	}  
Output:parent class constructor invoked
       instance initializer block is invoked
       child class constructor invoked
________________________________________
Another example of instance block
1.	class A{  
2.	A(){  
3.	System.out.println("parent class constructor invoked");  
4.	}  
5.	}  
6.	  
7.	class B3 extends A{  
8.	B3(){  
9.	super();  
10.	System.out.println("child class constructor invoked");  
11.	}  
12.	  
13.	B3(int a){  
14.	super();  
15.	System.out.println("child class constructor invoked "+a);  
16.	}  
17.	  
18.	{System.out.println("instance initializer block is invoked");}  
19.	  
20.	public static void main(String args[]){  
21.	B3 b1=new B3();  
22.	B3 b2=new B3(10);  
23.	}  
24.	}  
Output:parent class constructor invoked
       instance initializer block is invoked
       child class constructor invoked
       parent class constructor invoked
       instance initializer block is invoked
       child class constructor invoked 10
```
###### Note: first run static block-main method-static method

#### Rules of static block in Java
•	Static block always get executed before static method.
•	Static block cannot return a value.
•	Static block cannot be called explicitly.
•	Static block cannot throws an exception.
•	The this and super keywords cannot be used inside the static block.
•	If a class have multiple blocks then they will execute in the same order as they written.
#### When a static initializer block can be used
•	If you’re loading drivers. For ex, Class class has a static block where it registers the natives.
•	If you need to do manipulation in order to initialize your static variables, you can declare a static block which gets executed exactly once, when the class is first loaded.
•	If you need a Map with static values.
•	If you need some common values like server url, IP address at very beginning of the prg.
•	Security related issues or logging related tasks.
### Static keyword : 
SK in java is used for memory management mainly. We can apply java static keyword with variables (also known as class variable), methods (also known as class method), blocks and nested class. The static keyword belongs to the class than instance of the class.
•	The static variable can be used to refer the common property of all objects (that is not unique for each object) e.g. company name of employees,college name of students etc.
•	The static variable gets memory only once in class area at the time of class loading.
•	
•	A static method belongs to the class rather than object of a class.
•	A static method can be invoked without the need for creating an instance of a class.
•	static method can access static data member and can change the value of it.
•	
•	Static block used to initialize the static data member.
•	It is executed before main method at the time of classloading.

|INSTANCE/NON-STATIC VARIABLES|	STATIC VARIABLES|
| ------------- | ------------------------------ |
|1) An  instance  variable is  one  whose memory  space  is  creating  each  and every  time  whenever an  object  is created. | 1)  SV are  whose  memory space is creating only once when the class  is  loaded by class  loader subsystem(a part of JVM) in the main memory  irrespective of  number  of objects.|
|2) declaration  should  not  be  preceded by keyword static. Data type v1, v2…vn; |	2)  Programmatically  SV declaration  must  be  preceded  by keyword static. Static data type v1, v2…vn; |
|3)  Instance  variable must  be  accessed with  respect  to  object name  i.e., objname.varname;|3)  Static  variables must  be  accessed with  respect  to  class name  i.e., classname.varname;|
|4)  Value of  instance  variable is  not  sharable. |	4)  Value of  static  variable is  always recommended for sharable.| 
|5)  Instance  variable are  also  known  as object level data members since they are dependent on objects. |	5)  Static variableare also known as class level  data  members since  they  are dependent on classes|
### super() vs this():
The 1st line inside every constructor should be either super() or this() if we are not writing anything compiler will always generate super().
=>Can constructor perform other tasks instead of initialization Yes, like object creation, starting a thread, calling method etc. You can perform any operation in the constructor as you perform in the method.
#### this Keyword: 
###### this is a reference variable that refers to the current object.
1.	this keyword can be used to refer current class instance variable.
2.	this() can be used to invoke current class constructor.
3.	this keyword can be used to invoke current class method (implicitly)
4.	this can be passed as an argument in the method call.
5.	this can be passed as argument in the constructor call.
6.	this keyword can also be used to return the current class instance.
#### super Keyword:
###### The super keyword in java is a reference variable that is used to refer immediate parent class object. Whenever you create the instance of subclass, an instance of parent class is created implicitly i.e. referred by super reference variable.
1.	super is used to refer immediate parent class instance variable.
2.	Super () is used to invoke immediate parent class constructor.
3.	super is used to invoke immediate parent class method.
We can’t create object for abstract class but abstract class can contain constructor what is the need?
•	Abstract class constructor will be executed to perform initialization of child class object.

### Java Object Class Method.
clone() - Creates and returns a copy of this object.
equals() - Indicates whether some other object is "equal to" this one. 
finalize() - Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. 
getClass() - Returns the runtime class of an object. 
hashCode() - Returns a hash code value for the object.
 notify() - Wakes up a single thread that is waiting on this object's monitor.
 notifyAll() - Wakes up all threads that are waiting on this object's monitor. 
toString() - Returns a string representation of the object.
 wait() - Causes current thread to wait until another thread invokes the notify() method or the notifyAll() method for this object. 
### Abstract Method 
A method that is declared as abstract and does not have implementation is known as abstract method.Ex. abstract void printStatus();//no body and abstract  

### Abstract Class
Abstract classes are classes that contain one or more abstract methods. An abstract method is a method that is declared, but contains no implementation.
USE: An abstract class can be used as a type of template for other classes. The abstract class will hold common functionality for all classes that extend it.
### Abstract Class
1.	Abstract classes may or may not contain abstract methods, i.e., methods without body ( public void get(); )
2.	But, if a class has at least one abstract method, then the class must be declared abstract.
3.	If a class is declared abstract, it cannot be instantiated
4.	It can have constructors and static methods also.
5.	It can have final methods which will force the subclass not to change the body of the method.
6.	If a class have abstract methods, then the class should also be abstract using abstract keyword, else it will not compile.
7.	It’s not necessary for an AC to have abstract method. We can mark a class as abstract even if it doesn’t declare any abstract methods.

###### For example: Abtract Class Animal 
All animals move and breathe and reproduce so these can be put into the Animal Class.
Now Concrete Class Dog, Cat etc.

### Interface 
An interface is a collection of abstract methods. A class implements an interface, thereby inheriting the abstract methods of the interface. OR

interfaces can have abstract methods and variables. It cannot have a method body.

An interface can contain set of abstract methods. In an interface we cannot provide method with body. By default all the methods in an interface are “Abstract”.As part of an interface we can declare the variable ,  when we declare variables in the interface, by default they are “static and final” variables
o	Java 8, we can have default and static methods in an interface. Java 9, we can have private methods in an interface.
o	 It is used to achieve abstraction.I support the functionality of multiple inheritance.
o	It can be used to achieve loose coupling.
###### Qu. When we should go for interface, abstract class and concrete class?
•	When use=== >If you think you will need to add methods in the future, then an abstract class is a better choice. Because if you add new method headings to an interface, then all of the classes that already implement that interface will have to be changed to implement the new methods. That can be quite a hassle.
•	Interfaces are a good choice when you think that the API will not change for a while.
### Difference between interface and abstract class :
|Interface|	Abstract class|
| ------------- | ------------- |
|1)	If we don’t’ know anything about impl just we have requirement specification then we should go for interface.|	1)	If we are talking about impl but not completely (partial implementation) then we should go for abstract class.|
|2)	method present inside I is always public and abstract whether we are declaring or not.(default and static method also in jdk 1.8)|	2)	Every method present inside abstract class need not be public and abstract.|
|3)	We can’t declare interface methods with the modifiers private, protected, final,static,synchronized,nativestrictfp|	3)	There are no restrictions on abstract class method modifiers.|
|4)	Every interface variable is always public static final whether we are declaring or not.	|4)	Every abstract class variable need not be public static final.|
|5)	Every interface variable is always public static final we can’t declare with the following modifiers. Private, protected, transient, volatile.|	5)	There are no restrictions on abstract class variable modifiers.|
|6)	For the I variables compulsory we should perform initialization at the time of declaration otherwise we will get compile time error.|	6)	It is not require to perform initialization for abstract class variables at the time of declaration.|
|7)	Inside interface we can’t take static and instance blocks,main method.|	7)	Inside abstract class we can take both static and instance blocks,main method.|
|8)	Inside interface we can’t take constructor.|	8)	Inside abstract class we can take constructor.|
|9)	Interface can't provide the implementation of abstract class.|	9) Abstract class can provide the implementation of interface.|
|10)	Support multiple inheritance|	10) not support multiple inheritance|
|11)Interface can extends any no of interface at atime|	11) abstract class can extend only one class or one abstract class at a time|

### OOPS SOLID PRINCIPLES
##### SRP    OCP   LSP    ISP     DIP
###### S: Single responsibility principle: “One class should have one and only one responsibility”
######  O: Open-closed: “S/W components should be open for extension, but closed for modification” dispatcher servlet in spring and structts extends action
######  L: Liskov substitution principle: “Derived types must be completely substitutable for their base types”--properityEditor in spring
######  I: Interface segregation principle: “Clients should not be forced to implement unnecessary methods which they will not use” listner awt
######  D: Dependency inversion principle:“Depend on abstractions, not on concretions” bean cfg spring
