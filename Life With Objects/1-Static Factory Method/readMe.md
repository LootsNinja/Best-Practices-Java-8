# Creating and Destroying Objects
## Consider static factory methods instead of constructors

This approach is commonly agreed between experienced developers. The purpose of the approach is actually quite simple. 
When you need to create many contructors in your class which can be called telescoping or not sometimes, you better consider using
static factory methods. 

### Advantages:
* Static factory method is not the same as Factory Method design pattern.
* Because static factory methods have names, it is better and easier to use than constructors.
* No need to create new objects everytime they are invoked.
  * There can be instance-controlled classes thanks to static factory method approach.
  * Using static factory methods in interfaces since Java 8 can provide us creating very compact APIs.
* Any subtype of the declared return type is permissible.
  * The class of the returned object can vary from call to call as a function of the input parameters.
  * Not only the bulk of the API is reduced, but the conceptual weight as well. (the number and difficulty of the conceps that programmers must master in order to use the API.)
  * Using static factory method requires the clinet to refer to the returned object by interface rather than implementation class.
* The class of the returned objects doesn't need to exist when the class containing the method is written.


:bulb: The main limitation of providing only static factory methods is that classes without public or protected constructors cannot be subclassed.
