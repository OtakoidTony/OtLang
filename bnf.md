```bnf
<digit> ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
<letter> ::= "A" | "B" | "C" | "D" | "E" | "F"
<number> ::= <digit> | <letter>
<integer> ::= <number> | <number><integer>
```


## 변수 정의
이름:type=타입, value=값
```
<decl_var> ::= <identifier> ":" "type" "=" <type> ("," "value" "=" <expr>)? ";"
```
### example
x:type=int, value=3141592;
y:type=str, value="로지꾸";

## 함수 정의
```
<function_expr> ::= "box" <identifier> ":" NEWLINE
    "input" ":" NEWLINE (<decl_var>*)? NEWLINE
    "run" ":" NEWLINE <sentence>* NEWLINE
    ("output" ":" NEWLINE (<decl_var>*)? NEWLINE)?
    
```


## 조건문 정의

```
<if> ::= "logic" "(" <expr> ")" "{" <sentence>* "}"
    ("else" "if" "(" <expr> ")" "{" <sentence>* "}")*
    ("else" "{" <sentence>* "}")?
```

## 반복문 정의
```
<while> ::= "while" "(" <simple_sentence> ")"
    "{" <sentence>* "}"
    ("done" "{" <sentence>* "}")?
    ("else" "{" <sentence>* "}")?

<for_basic> ::= <decl_var> ";" <expr> ";" <simple_sentence>
<for_iter> ::= <decl_var> "in" <expr>

<for> ::= "for" "(" <for_basic> | <for_iter> ")"
    "{" <sentence>* "}"

```
