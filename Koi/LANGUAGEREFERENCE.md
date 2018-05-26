# Koi Language Reference
The language reference for the Koi language.

## Keywords
- `true` - Boolean
- `false` - Boolean
- `var` - Mutable Variable Assignment Initiation
- `val` - Immutable Variable Assignment Initiation
- `none` - Nothing
- `cha` - Character
- `str` - String
- `int` - Integer
- `flo` - Float
- `boo` - Boolean
- `dyn` - Dynamic
- `if` - If
- `elf` - Else If - Using the keyword "elf" for "else if" layers the if statement in a staircase-like fashion.
- `else` - Else
- `for` - For
- `in` - In
- `while` - While
- `fun` - Function
- `pro` - Procedure
- `meth` - Method - Methods exist only with-in classes, so the keyword uses 4 letters to distance it from functions and procedures.
- `class` - Class
- `object` - Object
- `pub` - Public
- `prv` - Private
- `extern` - External/Static
- `intern` - Internal/Protected
- `fin` - Final
- `const` - Constant
- `pass` - Pass
- `return` - Return
- `continue` - Continue
- `del` - Delete (deletes an object in the current scope)
- `magic` - Magic (things that exist in the compiler/interpreter)
- `native` - Native (something wrapping C code)
- `import` - Import
- `from` - From

## Symbols
- `+` - Addition
- `-` - Subtraction
- `*` - Multiply
- `/` - Divide
- `//` - Float Division
- `=` - Value Assignment
- `:=` - Inferred Type Value Assignment
- `=+` - Equals Plus
- `=-` - Equals Minus
- `=*` - Equals Multiply
- `=/` - Equals Divide
- `=//` - Equals Float Divide
- `~` - Roughly
- `.` - Object Accessor
- `..` - Range
- `...` - Var Args
- `@` - Reverse Object Accessor/Attribute On
- `@!` - Attribute Off
- `"` - Non-Literal String
- `'` - Literal String
- Backtick - Multi-line String
- `()` - Function Call/Class Constructor
- `,` - Parameter Separation
- `==` - Equal To
- `<=` - Less Than Or Equal To
- `>=` - More Than Or Equal To
- `<>` - Less Than Or More Than
- `<=>` - Less Than Or Equal To Or More Than
- `!=` - Not Equal To
- `!` - Not/Ignores Keyword
- `<` - Less Than
- `>` - More Than
- `^` - Throw Error
- `:` - Type Assignment/Ratio
- `->` - Return Type

## File Extensions
Koi, unlike other languages, uses different file extensions for its' files. Different extensions are not needed, but are there to help identify what the file contains before it is opened.
- `koi` - (used for any piece of code outside of a class, function, etc, or multiple types; a function and a class)
- `ks` - Koi Subroutine (used for files that contain just a subroutine)
- `kp` - Koi Procedure (used for files that contain just a procedure)
- `kf` - Koi Function (used for files that contain just a function)
- `kc` - Koi Class (used for files that contain just a class)
- `ko` - Koi Object (used for files that contain just a singleton)
- `km` - Koi Macro (used for files that contain just a macro)
- `kr` - Koi Reference (used for out-of-code documentation)
- `kl` - Koi Library (used for libraries)

## Sub-Routines
All of the sub-routines can be called like so:
```
{id}({parameters*})
```
## Subroutine
A subroutine is a function that works in the global scope.
```
sub mySubroutine({parameters*}) {block}
sub mySubroutine({parameters*}) -> {type} {block}
```
### Procedures
A procedure is a function that does not have a return value. Procedures lack the ability to return anything, so an error will be raised if a variable is assigned to a procedure call.
```
pro myProcedure({parameters*}) {block}
```
### Functions
A function can be called with a defined set of parameters. The parameter names, types and optional values are defined with the functions and the values are defined when the function is called. If the return type is not specified, it will be "none".
```
fun myFunction({parameters*}) {block}
fun myReturn({parameters*}) -> {type} {block}
```
### Methods
A method is a function that belongs to a class, they have their own scope but can also work with the class scope.
```
meth myMethod({parameters*}) {block}
meth myReturn({parameters*}) -> {type} {block}
```
### Parameters
Parameters are used in sub-routine declaration and are then used from the sub-routine. The type and default value of a parameter are optional.

The most basic form of a parameter is just an ID.
```
{id}

my_id
```
However, the type of the parameter may also be specified.
```
{id}: {type}

my_id: str
```
A default value for the parameter can be defined, either on its' own or with the type.
```
{id} := {default value}
{id}: {type} = {default value}

my_id := "string"
my_id: str = "string"
```
The last parameter may also have an ellipsis after the ID, making that parameter into a list of the given type. The parameter will now no longer be able to accept a default value. The function call will now accept an endless amount of values, with the extra values being passed into the parameter with an ellipsis.
```
{id}...
{id}: {type}...

my_id...
my_id: str...
```

## Classes
Classes are objects that can contain variables and methods. Classes can be extended from other classes, carrying over the extended classes' variables and methods. Methods from the extended classes' can then be overridden in the new class.
```
class MyClass({extensions*}) {block}
```

## Variables
Variables are names that are attached to values. The variables available depend on the current scope. Variables can be defined as mutable with "`var`" or as final with "`val`".
```
var my_var: {type} = {value}
val my_val: {type} = {value}
```
The value of the variable is optional, if not specified, it will be "none" or the smallest it could be for the specified type - 0 for an integer. The type, however, must either be specified or the following syntax must be used:
```
var my_var := {value}
val my_val := {value}
```

## Statements
### If
An if statement is used to compare values with others. An if statement can optionally be followed by an elf and/or else statements.
```
if ({boolean}) {}
```
#### Elf
An elf statement can only follow an if statement, and is run if the comparison in the if statement is false, but its' comparison is true.
```
if (...) {}
elf ({boolean}) {}
```
#### Else
An else statement can only follow an if or elf statement, and is run if the comparison in the if or elf statements were false.
```
if (...) {}
else {}

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
For loops can also be used to loop through multiple things, using commas for each loop.
```
for ({id} in {object with length}, {id} in {object with length}) {}
```
### While
A while loop will loop for as long as the comparison is true. As soon as it isn't, the loop will stop.
```
while ({boolean}) {}
```

## Operators
### Comparison
Comparison operators can be used to compare two values and return a boolean.
```
{value} {comparison operator} {value}
```
### Arithmetic
Arithmetic operators are used to perform mathematical functions on values.
```
{value} {arithmetic operator} {value}
```
