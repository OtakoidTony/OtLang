```bnf
<decl_func> ::= "." <identifier> NEWLINE
<command>   ::= <function> <variable>* ( <type> | <data> )? ( <;> | NEWLINE )
```

```asm
.func1
    MAK A STR ;변수 A를 만들고 타입은 문자열로 설정해라.
    MAK B STR
    MAK C INT ;변수 C를 만들고 타입은 정수로 설정해라.
    LET A "Hello World!" ;A의 값을 "Hello World!"이라 해라.
    LET B "Hello There!"
    LET C 3 ;C의 값을 3이라 해라.
    PSH A B ;A의 값을 B의 값으로 바꿔라.

.func2
    GET LOC A .func1 7 ;.func1 을 7번째줄까지 실행할 때 A의 값을 가져오고 .func2의 지역변수로서 할당을 해라.
    MAK B TYP A ;변수 B를 만들되 타입은 A와 같은 것으로 설정해라.
    
.func3
    MAK A INT
    MAK B INT
    MAK C BLN
    LET C [A > B];C의 값을 명제 A>B 이라 해라.
    CAS C TRU .func1 ;C가 참일 때, .func1를 실행해라.
    CAS C FAL .func2 ;C가 거짓일 때, .func2를 실행해라.
    
```

```asm
.func1
    MAK [A, B, C] [STR, STR, INT] ;변수 A와 B와 C를 만들고 타입은 각각 문자열, 문자열, 정수로 설정해라.
    LET A "Hello World!" ;A의 값을 "Hello World!"이라 해라.
    LET B "Hello There!"
    LET C 3 ;C의 값을 3이라 해라.
    PSH A B ;A의 값을 B의 값으로 바꿔라.

.func2
    GET LOC A .func1 7 ;.func1 을 7번째줄까지 실행할 때 A의 값을 가져오고 .func2의 지역변수로서 할당을 해라.
    MAK B TYP A ;변수 B를 만들되 타입은 A와 같은 것으로 설정해라.
```
