# Koi
The Koi programming language.

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
    for name in names {
        println("Hello #{name}!")
    }
}
```