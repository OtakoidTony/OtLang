# Otlang

모든 것이 input, run, output으로 돌아가는 언어, OtLang.  
function은 하나의 box객체로 취급하여 변수간의 상호작용이 가능.  
모든 객체는 선언시 변수에 대한 설명을 요구.  

지역변수와 전역변수는 global과 local를 직접 명시해주면 구분가능.  
box간의 연결을 통해 함수합성 구현.  

flag라는 변수를 이용하여 병렬처리를 실행하며, 줄단위 실행이 가능.


## flag란
flag는 일종의 방송과 같은 역활을 하며, flag가 발생시, 다른 함수에 영향을 미치는 것이 가능하다.  

```
box func:
    input:
        x: type = int
        y: type = bool
    run:
        if y:
            z=x*2
            temp: type =
                flag: "x*2"
            z=z*2
    output:
        z: type = int

arise func "x*2":
    run:
        print("arised!")

func 5 3

```


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
