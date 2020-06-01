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
- It is the process of Encapsulating data and corresponding methods into a single module.
- Encapsulation is a process of wrapping of data and methods in a single unit is called encapsulation.
- Encapsulation is achieved in java language by class concept.
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
###### To achieve encapsulation in Java: 
- Declare the variables of a class as private.
- Provide public setter and getter methods to modify and view the variables values.
- The Java Bean class is the example of fully encapsulated class.

### Polymorphism: (Adapter Dp):
Same name with different forms is the concept of polymorphism.Polymorphism is the ability of an object to take on many forms.The most common use of polymorphism in OOP occurs when a parent class reference is used to refer to a child class object.

###### Example 1:
We can use same abs() method for int type, long type, float type etc.
abs(int)   abs(long)    abs(float)
###### Example 2: 
We can use the same List reference to hold ArrayList object, LinkedList object, Vector object, or Stack object.
###### Example:

1)	List l=new ArrayList();
2)List l=new LinkedList();
3)List l=new Vector();
4) List l=new Stack();

The best exp  of polymorphism is, in our project we have implemented, build the response.If it is success we are calling one method buildResponse(obj.). If it is failure we will call same buildResponse(String respCode, String respMsg). But method parameter must be different.

 
1)	Inheritance talks about reusability.
2)Polymorphism talks about flexibility.
3)	Encapsulation talks about security.

### IS-A Relationship(inheritance):
1)	Also known as inheritance.
2)By using extends keywords we can implement IS-A relationship.
3)The main advantage of IS-A relationship is reusability.

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
•	Without existing container object if there is no chance of existing contained objects then the relationship between container object and contained object is called composition which is a strong association.
###### Example:
•	University consists of several departments whenever university object destroys automatically all the department objects will be destroyed that is without existing university object there is no chance of existing dependent object hence these are strongly associated and this relationship is called composition.
