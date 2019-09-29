# Otlang

모든 것이 input, run, output으로 돌아가는 언어, OtLang.  
function은 하나의 box객체로 취급하여 변수간의 상호작용이 가능.  
모든 객체는 선언시 변수에 대한 설명을 요구.  

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
