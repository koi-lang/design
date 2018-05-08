# Koi
The Koi programming language.

## Examples
### Hello World
```
println("Hello World!")
```

### Function
```
fun Hello() {
    println("Hello World!")
}

fun HelloTo(name: String) {
    println("Hello #{name}!")
}

fun HelloAll(*names: String) {
    for (name in names) {
        println("Hello #{name}!")
    }
}
```

### Variable
```
var myVar = "A string."
var myOtherVar: String = "A string."

val myVal = "A final string!"
```

### For Loop
```
for (i in 5..10) {
    println(i)
}

for (i in 1..10, j in 5..7) {
    println(i, j)
}
```

### Parameter Multiple Types
```
fun AddNums(one: int || str, two: int || str) -> int || str {
    return int(one) + int(two)
}
```