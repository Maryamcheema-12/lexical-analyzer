# Nexus Pro: Advanced Lexical Analyzer & Mini C++ Compiler

A professional-grade **Lexical Analyzer** and **Syntax Guard** developed as a semester project for the **Compiler Construction** course. This tool simulates the front-end phases of a compiler, transforming raw C++ source code into a structured token stream and managing memory through a dynamic Symbol Table.

## 🎓 Project Context
* **Developer:** Maryam Naveed
* **Academic Level:** 7th Semester
* **Institution:** University of Central Punjab (UCP)
* **Course:** Compiler Construction

---

## 🚀 Core Features

### 1. Strict Lexical Analysis
The scanner reads C++ source code and categorizes lexemes into formal token classes using Deterministic Finite Automata (DFA) logic.
* **Keywords:** `int`, `while`, `if`, `return`, `cout`, etc.
* **Identifiers:** User-defined variable and function names.
* **Operators:** Arithmetic, Relational, and C++ specific operators like `<<` and `>>`.
* **Constants:** String literals and numeric values.

### 2. Professional Minification
Removes all "noise" from the source code to show the raw buffer passed to the parser:
* Eliminates single-line (`//`) and multi-line (`/* */`) comments.
* Removes redundant whitespaces and tabs.
* Compresses code into a single-line raw stream.

### 3. Smart Symbol Table & Memory Mapping
Unlike simple lists, this symbol table calculates **Memory Offsets** based on C++ data type sizes:
* **int/float:** 4 Bytes
* **double:** 8 Bytes
* **char/bool:** 1 Byte
* **string:** 24 Bytes (standard overhead)
* Generates sequential offsets (0, 4, 8, etc.) to simulate stack memory allocation.

### 4. Syntax & Terminator Guard
* **Bracket Matching:** Uses a Stack data structure to detect unbalanced `{ ( [` symbols.
* **Semicolon Detection:** Flags missing `;` at the end of statements with precise line numbers.

---

##  Technology Stack
* **Language:** Python 3.x
* **GUI Framework:** Tkinter (Custom Dark Theme)
* **NLP Library:** NLTK (for robust wordpunct tokenization)
* **Regex:** Python `re` module for DFA pattern matching

---

##  Interface Preview
The IDE is divided into four main functional areas:
1. **Source Editor:** Full-featured text area for writing C++ code.
2. **Token Stream:** Real-time table showing Lexemes and their Categories.
3. **Symbol Table:** Detailed map of variables, their types, and memory offsets.
4. **Terminal Output:** Displays the minified raw buffer and syntax error logs.

---

##  How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/Maryamcheema-12/lexical-analyzer.git](https://github.com/Maryamcheema-12/lexical-analyzer.git)
Install dependencies:

Bash
pip install nltk
Run the application:

Bash
python main.py
