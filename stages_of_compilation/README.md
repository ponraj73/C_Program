# Stages of Compilation in C

When a C program is executed, it does not directly convert into machine code.
The program goes through multiple stages before execution.

The main stages are:

1. Preprocessor
2. Compiler
3. Assembler
4. Linker

---

# Flow of Compilation

```text
source.c
   ↓
Preprocessor
   ↓
Expanded Source Code
   ↓
Compiler
   ↓
Assembly Code
   ↓
Assembler
   ↓
Object File
   ↓
Linker
   ↓
Executable File
```

---

# 1. Preprocessor

The **preprocessor** processes all the preprocessor directives before actual compilation.

### Works Performed

* Expands header files
* Replaces macros
* Removes comments
* Handles conditional compilation

### Example

```c id="tw3h5x"
#include <stdio.h>

#define VALUE 10
```

After preprocessing:

```c id="nq0o9x"
// Contents of stdio.h added

int x = 10;
```

### Output File

Usually generates:

```text
file.i
```

---

# 2. Compiler

The **compiler** converts the preprocessed C code into assembly language.

It checks:

* Syntax errors
* Semantic errors
* Type checking
* Optimization

### Example

C Code:

```c id="f4k0cf"
int a = 5 + 3;
```

Converted into Assembly Code:

```assembly id="lzw9xn"
MOV R0, #5
ADD R0, #3
```

### Output File

Usually generates:

```text
file.s
```

---

# 3. Assembler

The **assembler** converts assembly language into machine-level object code.

Machine code contains binary instructions understood by the processor.

### Example

Assembly:

```assembly id="jlwmzc"
MOV R0, #5
```

Machine Code:

```text
10110000
```

### Output File

Usually generates:

```text
file.o
```

(Object File)

---

# 4. Linker

The **linker** combines:

* Object files
* Library files
* Header-related implementations

to create the final executable file.

It also resolves function addresses and external references.

### Example

If we use:

```c id="gq2hha"
printf("Hello");
```

The linker connects the program with the standard library implementation of `printf()`.

### Output File

```text
a.out
```

or

```text
program.exe
```

---

# Simple Explanation of Each Stage

| Stage        | Purpose                          | Output           |
| ------------ | -------------------------------- | ---------------- |
| Preprocessor | Processes directives and macros  | `.i`             |
| Compiler     | Converts C code to assembly code | `.s`             |
| Assembler    | Converts assembly to object code | `.o`             |
| Linker       | Creates final executable file    | `.exe` / `a.out` |

---

# GCC Commands for Each Stage

## Preprocessing

```bash id="6g8gq3"
gcc -E file.c -o file.i
```

## Compilation

```bash id="99k1jv"
gcc -S file.i -o file.s
```

## Assembling

```bash id="6ljdb0"
gcc -c file.s -o file.o
```

## Linking

```bash id="m7lv2v"
gcc file.o -o output
```

### Simple Command

```bash id="m7lv2v"
gcc --save-temps program -o program
```
