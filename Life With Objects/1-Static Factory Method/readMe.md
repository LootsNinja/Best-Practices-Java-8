## Consider static factory methods instead of constructors

This approach is commonly agreed between experienced developers. The purpose of the approach is actually quite simple. 
When you need to create many contructors in your class which can be called telescoping or not sometimes, you better consider using
static factory methods. 

* Static factory method is not the same as Factory Method design pattern.
* Because static factory methods have names, it is better and easier to use than constructors.
* There can be instance-controlled classes thanks to static factory method approach.
* Using static factory methods in interfaces since Java 8 can provide us creating very compact APIs.
* Any subtype of the declared return type is permissible.

:bulb: The main limitation of providing only static factory methods is that classes without public or protected constructors cannot be subclassed.
