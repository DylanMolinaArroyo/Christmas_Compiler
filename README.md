# Christmas Compiler

## Description

**Christmas Compiler** is an academic compiler project that implements the three fundamental phases of compilation: **lexical analysis, syntactic analysis, and semantic analysis**. The compiler is built in **Java** and uses **JFLEX** for lexical analysis and **Java CUP** for parser generation. The project validates source programs, constructs and manages a symbol table, performs semantic checks, and reports errors in a structured and informative way.

This project was developed as part of a **Compiler Construction / Computer Engineering** course and focuses on correctness, clarity of structure, and separation of compilation stages.

---

## Features

* **Lexical Analysis (Scanner)**

  * Implemented using **JFLEX**
  * Tokenizes the input source code
  * Detects and reports lexical errors

* **Syntactic Analysis (Parser)**

  * Implemented using **Java CUP**
  * Validates grammar rules
  * Generates parsing actions and detects syntax errors

* **Semantic Analysis**

  * Symbol table management
  * Type checking
  * Validation of variable declarations and usage
  * Operator and expression validation
  * Detection of semantic errors such as:

    * Undeclared identifiers
    * Type incompatibilities
    * Invalid operations

* **Symbol Table Output**

  * Generates a structured representation of symbols
  * Useful for debugging and academic evaluation

---

## Project Structure

```
Christmas_Compiler/
│
├── src/
│   ├── JFLEX/
│   │   ├── Lexer.jflex       # Lexical specification
│   │   ├── Lexer.java        # Generated lexer
│   │   └── Lexer.class
│   │
│   ├── CUP/
│   │   ├── Parser.cup        # Grammar specification
│   │   ├── Parser.java       # Generated parser
│   │   ├── sym.java          # Token definitions
│   │   └── sym.class
│   │
│   ├── Clases/
│   │   ├── Semantico.java            # Semantic analysis logic
│   │   ├── TablaSimbolos.java        # Symbol table management
│   │   ├── Simbolo.java              # Symbol representation
│   │   ├── TipoDatos.java            # Data type definitions
│   │   ├── Funciones.java            # General semantic helpers
│   │   └── FuncionesOperadores.java  # Operator validation
│   │
│   ├── Traductor/
│   │   └── Traductor.java     # Translation / intermediate handling
│   │
│   ├── Main.java              # Program entry point
│   └── Prueba.txt             # Sample input program
│
├── salida.txt                 # Compilation output
├── salida_simbolos.txt        # Symbol table output
└── README.md
```

---

## Technologies Used

* **Java**
* **JFLEX** – Lexical analyzer generator
* **Java CUP** – LALR parser generator
* **IntelliJ IDEA** (project structure included)

---

## How It Works

1. The source code is read from an input file (e.g., `Prueba.txt`).
2. The **Lexer** scans the input and generates tokens.
3. The **Parser** validates the token sequence using grammar rules.
4. The **Semantic Analyzer**:

   * Builds and manages the symbol table
   * Performs type and scope validation
   * Detects semantic inconsistencies
5. Results and errors are written to output files:

   * `salida.txt`
   * `salida_simbolos.txt`

---

## How to Run

1. Open the project in **IntelliJ IDEA** or any Java-compatible IDE.
2. Ensure JFLEX and Java CUP generated files are present.
3. Compile the project.
4. Run `Main.java`.
5. Review the generated output files for results and errors.

---

## Academic Purpose

This project is intended for **educational use** and demonstrates:

* Compiler architecture
* Practical usage of lexer and parser generators
* Semantic analysis design
* Symbol table implementation

---

## License

This project is for **academic and educational purposes only**.

---

## Author

Developed as part of a Computer Engineering / Compiler Construction course by Fabricio Alfaro & Dylan Molina.
