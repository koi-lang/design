# Koi
The Koi programming language.

## Keywords
- `true`
- `false`
- `var`
- `none`
- `char`
- `str`
- `int`
- `float`
- `bool`

## Symbols
- `+` - Addition
- `-` - Subtraction
- `*` - Multiply/Endless Value Parameter
- `/` - Divide
- `:` - Value Assignment
- `.`
- `"` - Non-Literal String
- `'` - Literal String
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