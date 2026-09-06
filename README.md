# 🚀 Master C Programming: Complete Foundations Guide

Welcome to the **Learn C** repository! This open-source collection serves as a comprehensive notebook and reference guide for learning C from scratch. Whether you are stepping into system-level programming for the first time or looking for a structured cheat sheet, this repository covers fundamental concepts, core syntax, memory structures, and practical examples.

---

## 📌 1. Introduction to C

Developed by **Dennis Ritchie** at Bell Laboratories between 1972 and 1973, C is one of the most foundational programming languages in computer science. It was originally designed to build the Unix operating system.

### Why Learn C Today?
* **Direct Hardware Interaction:** C provides low-level memory access via pointers, making it ideal for systems programming.
* **Exceptional Performance:** C compiles down to native machine code with zero runtime overhead or garbage collection pauses.
* **Foundation of Modern Software:** Major operating systems (Linux, macOS, Windows kernel), databases (PostgreSQL, SQLite), and web browsers (Chromium engine) are written largely in C or C++.
* **Core Language Concepts:** Mastering C gives you a deep, mechanics-level understanding of how CPU and RAM interact.

---

## 📚 2. Libraries & The C Standard Library

Pure C contains only 32 core keywords (`if`, `for`, `int`, `return`, etc.). It relies heavily on **Libraries** to extend its functionality. 

A library in C consists of two parts:
1. **Header Files (`.h`):** Declare function prototypes, constants, and macros (tells the compiler *what* exists).
2. **Implementation Files (`.c` / compiled binaries):** Contain the actual code execution logic (tells the compiler *how* it works).

### Essential Standard Libraries Reference:

| Header File | Name / Purpose | Common Functions |
| :--- | :--- | :--- |
| `<stdio.h>` | Standard Input/Output | `printf()`, `scanf()`, `fgets()`, `getchar()` |
| `<stdlib.h>` | Standard General Utilities | `malloc()`, `free()`, `exit()`, `atoi()`, `rand()` |
| `<string.h>` | String Handling | `strlen()`, `strcpy()`, `strcat()`, `strcmp()` |
| `<math.h>` | Mathematical Operations | `sqrt()`, `pow()`, `sin()`, `ceil()`, `floor()` |
| `<stdbool.h>` | Boolean Definitions | Introduces `bool`, `true`, and `false` (C99+) |
| `<limits.h>` | Implementation Constants | Defines limits like `INT_MAX`, `INT_MIN`, `CHAR_BIT` |

> 💡 **Preprocessor Directive Rule:** Using `#include <header.h>` instructs the preprocessor to pull code from standard system directories. Using `#include "header.h"` tells it to search your local project folder first.

---

## ⚙️ 3. The C Compilation Pipeline

Unlike interpreted languages (like Python or JavaScript), C is directly compiled into machine binary. Behind the scenes, `gcc hello.c` executes four sequential phases:

```text
  [ hello.c ] ── (1. Preprocessor) ──> [ Expanded Source (.i) ]
                                                │
                                         (2. Compiler)
                                                │
                                                ▼
  [ Machine Code / Binary ] <── (4. Linker) ── [ Assembly (.s) ]
           │                                    │
       (a.out / .exe)                    (3. Assembler)
                                                │
                                                ▼
                                       [ Object File (.o) ]
