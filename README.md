# Otlang


```
type number:
    int
    long
    float
    string
    bool
    complex

type otlang:
    make
    logic
    box

make a:
    input:
        none
    run:
        none
    output:
        a: type = int

logic isTrue:
    input:
        x: type = int
        y: type = int
    run:
        z= ? x>y
    output:
        z: type = bool

box func:
    input:
        x: type = int
        y: type = bool
    run:
        if y: z=x*2
    output:
        z: type = int
```
