# Creating and Destroying Objects
## Consider a builder pattern when faced with many constructor parameters

Static factories and constructors share a limitation: they do not scal well to large number of optional parameters.

:grey_exclamation: A telescoping constructor pattern works, but its hard to write clinet code when there are many parameters, and harder to read it.

:grey_exclamation: JavaBeans pattern solves the issue by calling a parameterless constructure to create the object and then call setter methods to set each required parameter and each optional parameter of interest.
* Disadvantages:
  * construction is split across multiple calls, a JavaBean may be in an inconsistent state partway through its construction.
  * The calss does not have the option of enforcing consistency.

## Builder Pattern
### Advantages:
* The client code is easy to write and easy to read. (The builder pattern simulates named optional parameters)
* The builder pattern is well suited to class hierarchies.
* Builders can have multiple varargs parameters because each parameter is specified in its own method.
* The builder pattern is quite flexible.

### Limitations:
* In order to create an object, you must first create its builder.
* Builder pattern is more verbose than the telescoping constructor pattern. (it must be used only if there are enough paramters to make it worthwhile)

:bulb: The builder pattern is a good choice when designing classes whose constructors or static factories would have more than a handful of parameters, especially if many of the parameters are optional or identical type.
