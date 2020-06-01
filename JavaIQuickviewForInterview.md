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
To achieve encapsulation in Java: Declare the variables of a class as private.
Provide public setter and getter methods to modify and view the variables values. The Java Bean class is the example of fully encapsulated class.
