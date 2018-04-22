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
## Statements
### If
An if statement is used to compare values with others. An if statement can optionally be followed by an elf and/or else statements.
```
if ({value} {comparison operator} {value}) {}
```
#### Elf
An elf statement can only follow an if statement, and is run if the comparison in the if statement is false, but its' comparison is true.
```
if (...) {}
elf ({value} {comparison operator} {value}) {}
```
#### Else
An else statement can only follow an if or elf statement, and is run if the comparison in the if or elf statements were false.
```
if (...) {}
elf (...) {}
else {}
```
## Loops
### For
For loops will loop for as long as there is another item in the given object with length, the value of the given id will be set to the value of the current item in the object with length.
```
for ({id} in {object with length}) {}
```
### While
A while loop will loop for as long as the comparison is true. As soon as it isn't, the loop will stop.
```
while ({value} {comparison operator} {value}) {}
```
