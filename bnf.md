```bnf
<digit> ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
<letter> ::= "A" | "B" | "C" | "D" | "E" | "F"
<number> ::= <digit> | <letter>
<integer> ::= <number> | <number><integer>
```


## 변수정의
var 이름 [as 타입] [= 초기화값]; 
```
<decl_var> ::= "var" <identifier> ("as" <type>)? ("=" <expr>)? ";"
```

## 함수정의
```
<function_expr> ::= "function" "(" (<name_type> ( "," <name_type>)*)? ")" ("as" <type>)?
    "{" <sentence>* "}"
```




```
<if> ::= "logic" "(" <expr> ")" "{" <sentence>* "}"
    ("else" "if" "(" <expr> ")" "{" <sentence>* "}")*
    ("else" "{" <sentence>* "}")?
    
<while> ::= "while" "(" <simple_sentence> ")"
    "{" <sentence>* "}"
    ("done" "{" <sentence>* "}")?
    ("else" "{" <sentence>* "}")?

<for_basic> ::= <decl_var> ";" <expr> ";" <simple_sentence>
<for_iter> ::= <decl_var> "in" <expr>

<for> ::= "for" "(" <for_basic> | <for_iter> ")"
    "{" <sentence>* "}"

```
