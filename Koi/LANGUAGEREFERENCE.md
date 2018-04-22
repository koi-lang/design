# Koi
The language reference for the Koi language.

## Sub-Routines
### Procedures
A procedure is function that works in with the global scope.
```
pro MyProcedure({parameters*}) {}
```
### Functions
A function can be called with a defined set of parameters. The parameter names, types and optional values are defined with the functions and the values are defined when the function is called.
```
fun MyFunction({parameters*}) {}
```
### Methods
A method is a function that belongs to a class, they have their own scope but can also work with the class scope.
```
met MyMethod({parameters*}) {}
```
### Parameters
Parameters are used in sub-routine declaration and are then used from the sub-routine. The type and default value of a parameter are optional.
```
{id} -> {type}: {default value}
```
## Classes
Classes are objects that can contain variables and methods. Classes can be extended from other classes, carrying over the extended classes' variables and methods. Methods from the extended classes' can then be overridden in the new class.
```
class MyClass({extensions*}) {}
```
### Private Block
The private block exists only with-in a class and is used to define private variables and methods.
```
private {}
```
### Public Block
The public block exists only with-in a class and is used to define public variables and methods.
```
public {}
```
### Static Block
The static block exists only with-in a private or public block and is used to define static variables and methods.
```
static {}
```
## Variables
Variables are names that are attached to values. The variables available depend on the current scope. Variables can be defined as mutable with "`var`" or as final with "`val`". The type and value of the variable is optional (variables will equal `none` if not given a value).
```
var myVar -> {type}: {value}
val myVal -> {type}: {value}
```
