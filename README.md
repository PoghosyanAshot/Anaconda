📘 README.md — Anaconda-Like Interpreter in C

Below is the full, ready-to-use README — no placeholders, fully tailored to your exact project structure and features.

# 🐍 Anaconda-Like Programming Language Interpreter (C)

This project is a fully implemented **programming language interpreter**, written entirely in **C**, featuring:

- Custom **tokenizer (lexer)**
- Hand-written **recursive-descent parser**
- A complete **AST (Abstract Syntax Tree)**
- **Interpreter** with:
    - Variables
    - Assignments
    - Arithmetic expressions
    - Strings
    - Boolean expressions
    - `if / else`
    - `while`
    - `for`
    - `{ blocks }`
    - `print()`
- Dynamic **symbol table** (variables stored at runtime)

This is a minimal but fully working language similar to Python/JavaScript, built from scratch for educational and experimental purposes.

---

## 🚀 Features

### ✔ Tokenizer (Lexer)

Supports:

- Identifiers
- Numbers
- Strings
- Keywords: `tiv`, `sahox`, `tox`, `print`, `ete`, `kam`, `while`, `for`
- Operators:
    - Arithmetic: `$` (add), `~` (sub), `#` (mul), `@` (div)
    - Logical: `< > <= >= == !=`
    - Assignment: `=`
- Punctuation: `; , ( ) { }`

---

### ✔ Parser (AST Builder)

Implements:

- Variable declarations
- Assignments
- Binary expressions
- Parentheses
- Blocks `{ ... }`
- Conditional statements
- Loops (`while`, `for`)
- Print statements
- Full expression grammar with precedence

---

### ✔ Interpreter

Executes AST using:

- Symbol table
- Value system (`number`, `string`, `bool`, `null`)
- Truthiness evaluation
- Execution engine for AST nodes

---

## 📄 Example Program

Your language supports **variables, loops, if statements, and printing**.

Example:

```txt
tiv x = 0;
while (x < 5) {
    print(x);
    x = x $ 1;
}


Example with strings:

tox msg = "Hello World!";
print(msg);


Example with if / else:

tiv a = 10;
ete (a > 5) {
    print("big");
} kam {
    print("small");
}


Example for loop:

for (tiv i = 0; i < 3; i = i $ 1) {
    print(i);
}

🛠 Build & Run
1. Compile:
gcc -o interpreter main.c


(If your file is not main.c, change the name.)

2. Run with source code:
./interpreter program.txt

📁 Project Structure
├── interpreter.c        # Full implementation (lexer, parser, AST, interpreter)
├── README.md
└── examples/
    ├── loops.txt
    ├── strings.txt
    ├── conditions.txt
    └── variables.txt

🔍 Internal Architecture Overview
1. Lexer

Splits file into tokens using:

tokenizing()

createAndpushToken()

Handles:

Multi-char operators (==, !=, <=, >=)

String literals

Keywords

2. Parser

Recursive descent parser:

parseStatement()

parseExpression()

parseAssignmentExpression()

parseIfStatement()

parseWhileStatement()

parseForStatement()

parseBlock()

Produces a full Abstract Syntax Tree.

3. AST Node Types

Includes:

NODE_TYPE_NUMBER
NODE_TYPE_STRING
NODE_TYPE_VARIABLE
NODE_TYPE_ASSIGNMENT
NODE_TYPE_VAR_DECL
NODE_TYPE_BINARY_OP
NODE_TYPE_PRINT
NODE_TYPE_IF
NODE_TYPE_WHILE
NODE_TYPE_FOR
NODE_TYPE_BLOCK

4. Interpreter

Executes all node types with:

executeStatement()

executeProgram()

evaluateExpression()

Symbol table with:

define

assign

lookup

🧪 Example Errors

Your interpreter detects:

Unknown tokens

Missing semicolons

Unterminated strings

Assignment to non-variables

Undeclared variable access

Missing braces or parentheses

Example:

Error on line 5. Expected ';' character.

🎯 Goals of the Project

This project is designed to teach:

How interpreters work internally

How lexers & parsers operate

How AST execution is performed

How to build your own programming language

How to implement dynamic memory structures in C

It is ideal for students learning:

Compiler theory

Programming language design

C memory management

Parser construction

🏆 Future Improvements

Planned upgrades:

Functions

Arrays

Objects

Return statements

Scopes (stack of symbol tables)

Error recovery (instead of exit)

Bytecode compiler + VM backend

Garbage collector

📜 License

MIT License — free for study, modification, and research.

If you want, I can also create:

✅ Logo for the language
✅ Syntax highlighting file
✅ Examples folder with real programs
✅ YouTube-style explanation text
✅ PDF documentation
```
