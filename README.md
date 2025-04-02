# Monkey Programming Language - v0.1.0

This repository contains the source code for a simple interpreted programming language written in Go, called Monkey.  This release is a basic implementation focused on demonstrating core concepts of interpreter design based in the book "Writing An Interpreter in Go" by Thorsten Ball.

## Interesting Techniques

This project utilizes several key techniques common in interpreter and compiler design:

* **Recursive Descent Parsing:** The parser uses a recursive descent approach to build an Abstract Syntax Tree (AST) from the token stream.  You can find more information on parsing techniques [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch).  See the `parser` directory for implementation details.
* **Lexer (Scanner):** A lexer breaks down the source code into a stream of tokens. Our lexer uses regular expressions for efficient tokenization. The `lexer` directory contains the code. [Learn more about lexing](https://en.wikipedia.org/wiki/Lexical_analysis).
* **Abstract Syntax Tree (AST):** The parser creates an AST, a tree representation of the code's structure, which is easier for the interpreter to process than the raw token stream.  See the `ast` directory. [Read about ASTs](https://en.wikipedia.org/wiki/Abstract_syntax_tree).
* **Object System:** Monkey has a simple object system implemented in the `object` directory, demonstrating basic object creation and manipulation.
* **Testing:** Comprehensive unit tests are included for the lexer, parser, and evaluator using Go's built-in testing framework. See the `*_test.go` files in each relevant directory.

## Libraries

This project leverages Go's built-in features extensively, with no external libraries beyond the standard library.  The focus is on demonstrating core concepts clearly.

## Project Structure

```
├── token
│   └── token.go
├── evaluator
│   ├── evaluator_test.go
│   ├── builtins.go
│   └── evaluator.go
├── go.mod
├── LICENSE
├── lexer
│   ├── lexer_test.go
│   └── lexer.go
├── repl
│   └── repl.go
├── parser
│   ├── parser_test.go
│   └── parser.go
├── README.md
├── .gitignore
├── object
│   ├── object.go
│   ├── environment.go
│   └── object_test.go
├── ast
│   ├── ast_test.go
│   └── ast.go
└── .git

```

* **`token`**: Defines the token types used by the lexer.
* **`lexer`**:  Implements the lexical analyzer (lexer or scanner).
* **`parser`**: Implements the recursive descent parser.
* **`ast`**: Defines the structure of the Abstract Syntax Tree (AST).
* **`object`**: Defines the different object types within the Monkey language.
* **`evaluator`**: Implements the interpreter that evaluates the AST.
* **`repl`**:  Implements a simple Read-Eval-Print Loop (REPL) for interactive use.

## How to Use

1. **Clone the repository:** `git clone https://github.com/raziel-aleman/monkey-go.git`
2. **Navigate to the directory:** `cd monkey-go`
3. **Build:** `go build`
4. **Run:** `./monkey-go`

This will start the REPL. You can then type Monkey code and see the results.  Use `Ctrl+C` to quit.

## Future Work

Future versions will include features such as:

*  More robust error handling.
*  Improved built-in functions.
*  Support for more complex data structures.


This is a foundational project, ideal for understanding interpreter and compiler design principles.  Contributions are welcome!

