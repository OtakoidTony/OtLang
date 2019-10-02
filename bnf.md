# OtLang BNF Definition

## 변수 정의
```
<decl_var> ::= <identifier> ":" "type" "=" <type> ("," "value" "=" <expr>)? ";"
```
### example
```
x:type=int, value=3141592;
y:type=str, value="로지꾸";
```
## 함수 정의
```
<function_expr> ::= "box" <identifier> ":" NEWLINE
    "input" ":" NEWLINE (<decl_var>*)? NEWLINE
    "run" ":" NEWLINE <sentence>* NEWLINE
    ("output" ":" NEWLINE (<decl_var>*)? NEWLINE)?
    
```
### example
```
box function1:
    input:
        x:type=int
    run:
        x=x+1
    output:
        x:type=int
```
## 조건문 정의

```
<if> ::= "logic" "(" <expr> ")" "{" <sentence>* "}"
    ("branch" "logic" "(" <expr> ")" "{" <sentence>* "}")*
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
