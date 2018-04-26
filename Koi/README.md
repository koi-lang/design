# Koi
The Koi programming language.

## Keywords
- `true` - Boolean
- `false` - Boolean
- `var` - Variable Assignment
- `none` - Nothing
- `char` - Character
- `str` - String
- `int` - Integer
- `float` - Float
- `bool` - Bool
- `if` - If
- `elf` - Else If
- `else` - Else
- `for` - For
- `in` - In
- `while` - While
- `fun` - Function
- `pro` - Procedure
- `met` - Method
- `class` - Class
- `object` - Object

## Symbols
- `+` - Addition
- `-` - Subtraction
- `*` - Multiply/Endless Value Parameter
- `/` - Divide
- `:` - Value Assignment
- `.` - Object Accessor
- `..` - Range
- `@` - Reverse Object Accessor
- `"` - Non-Literal String
- `'` - Literal String
- Backtick - Multi-line String
- `()` - Function Call/Class Constructor
- `,` - Parameter Separation
- `=` - Equal Comparison
- `!` - Not/Ignores Keyword
- `<` - Less Than
- `>` - More Than
- `->` - Type Assignment

## Core Functions
- `print`
- `println`
- `input`
- `inputln`

## Examples
hello_world.koi
```
println("Hello World!")
```

function.koi
```
fun Hello() {
    println("Hello World!")
}
```

say_hello.koi
```
fun Hello(name -> String) {
    println("Hello #{name}!")
}
```

say_multiple_hello.koi
```
fun HelloAll(*names -> String) {
    for (name in names) {
        println("Hello #{name}!")
    }
}
```

variable_assignment.koi
```
var myVar: "A string."
```

for_loop.koi
```
for (i in 5..10) {
    println(i)
}

for (i in 1..10, j in 5..7) {
    println(i, j)
}
```