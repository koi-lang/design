# KIL
The Koi Intermediate Language.

## Examples
hello_world.kil
```
print "Hello World!"
newline
```

function.kil
```
.func Hello
    print "Hello World!"
    newline
.endfunc
```

say_hello.kil
```
# Given that the input was: "Frank"
.func Hello
    .local str name
    name = "Frank"
    print $name
    newline
.endfunc
```

say_multiple_hello.kil
```
# Given that the input was: "Frank", "Lewis"
.func HelloAll
    .local list names
    names = ["Frank", "Lewis"]
    
    LOOP1_INIT:
        .local int counter
        counter = 0
    
    LOOP1_TEST:
        if counter <= len names: goto LOOP1_BODY
        goto LOOP1_END
        
    LOOP1_BODY:
        print "Hello "
        print names[counter]
        newline
        
    LOOP_CONTINUE:
        inc counter
        goto LOOP_TEST

    LOOP1_END:
.endfunc
```