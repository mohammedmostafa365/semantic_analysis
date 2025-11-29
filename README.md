# 🐍 Semantic Analysis & AST Examples in Python

This repository contains multiple Python examples demonstrating **Abstract Syntax Tree (AST) creation** and **Semantic Analysis** for simple Python programs. These examples are intended for educational purposes, especially for compiler design and programming language concepts.

---

## 📝 Semantic Analysis (A Brief Explanation)

**Semantic Analysis** is a crucial phase in the compilation process that checks the **meaning** and **consistency** of the program code, following the lexical and syntax (parsing) phases. 

[Image of Compiler Phases Diagram]


It ensures the program adheres to the language's rules regarding **types**, **scope**, and **declarations**, detecting errors that are syntactically correct but logically flawed.

Key functions of semantic analysis include:

* **Type Checking:** Verifying that operators are applied to operands of compatible types (e.g., preventing the addition of an integer and a string: `5 + "hello"`).
* **Declaration/Scope Checking:** Ensuring that every **variable**, **function**, or **class** is **declared** before it is used and that it is being accessed within its correct **scope**.
* **Argument Checking:** Validating that function calls supply the correct number and types of arguments.
* **Symbol Table Management:** Building and updating a **Symbol Table**—a data structure that stores information about every identifier (like its type, scope, and definition location) to facilitate the checks above.

**Example Errors Detected:**

| Error Type | Python Example | Issue |
| :--- | :--- | :--- |
| **Undefined Variable** | `a = b + 1` | The variable `b` is used but never defined or declared in the current scope. |
| **Type Mismatch** | `z = 5 + "text"` | Trying to apply the `+` operator to incompatible types (`int` and `str`). |
| **Incorrect Function Call** | `my_func(x)` where `my_func` requires two arguments. | Mismatch between the expected and provided number of arguments. |

---

## Files & Examples

### 1. AST Printer for `sum_digits` function
-   **File:** `ast_sum_digits.py`
-   **Description:** Parses a recursive function `sum_digits(n)` into a Python AST and prints it hierarchically.  
-   **Note:** AST output examples are provided as images in the compressed folder.

### 2. AST + Semantic Analysis for factorial example
-   **File:** `ast_factorial.py`
-   **Description:** Builds a custom AST for a factorial function and performs a semantic check to validate function arguments (e.g., ensuring the input is non-negative).  
-   **Note:** AST and semantic output examples are provided as images in the compressed folder.

### 3. Semantic Analysis for variable operations
-   **File:** `semantic_vars.py`
-   **Description:** Demonstrates semantic analysis on variable assignments and type checking.  
-   **Note:** AST and semantic output examples are provided as images in the compressed folder.

### 4. Simple semantic analysis example
-   **File:** `semantic_simple.py`
-   **Description:** Simple example showing variable usage errors.  
-   **Note:** AST and semantic output examples are provided as images in the compressed folder.

---

## Requirements

-   Python 3.6+
-   [colorama](https://pypi.org/project/colorama/) (optional for colored output)

```bash
pip install colorama
