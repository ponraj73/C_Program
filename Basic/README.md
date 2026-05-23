# C Programming

## What is C? Why is it used?

C is a programming language developed in the 1970s by Dennis Ritchie at Bell Labs.

C is called a **middle-level language** because it supports both:

* **Low-level programming** → direct interaction with hardware
* **High-level programming** → easy-to-understand syntax for users

Because of this, C is widely used in:

* Embedded systems
* Operating systems
* Device drivers
* Microcontrollers
* System programming

---

# High-Level Language

High-level languages are easy for humans to read, write, and understand.

### Features

* Less coding effort
* Human-readable syntax
* Easier debugging and maintenance

### Examples

* C
* C++
* Java
* Python

---

# Low-Level Language

Low-level languages are closer to machine instructions and hardware.

### Features

* More coding effort
* Harder to understand
* Faster hardware interaction
* Used for direct hardware control

### Examples

* Assembly Language
* Machine Language

---

# Basic Structure of C

C is a **procedural programming language**, meaning the program executes step by step.

A **function** is a block of code that contains statements and logic to perform a specific task.

```c
// Comments

#include <stdio.h>   // Preprocessor directive and header file

// Global variables

// Function prototype
void display();

int main()
{
    // Statements

    display();

    return 0;
}

// Function definition
void display()
{
    printf("Hello World");
}
```

---

# Components of a C Program

## 1. Comments

Used to explain the code.

```c
// Single-line comment

/* Multi-line
   comment */
```

---

## 2. Preprocessor Directives

Used to include header files before compilation.

```c
#include <stdio.h>
```

---

## 3. Header Files

Contain predefined functions and macros.

Example:

```c
stdio.h
```

Used for input and output functions like:

```c
printf()
scanf()
```

---

## 4. Global Variables

Variables declared outside all functions.

```c
int a = 10;
```

They can be accessed throughout the program.

---

## 5. main() Function

Execution of a C program starts from the `main()` function.

```c
int main()
{
    return 0;
}
```

---

## 6. Function Prototype

Declares a function before its actual definition.

```c
void display();
```

---

## 7. Function Definition

Contains the actual implementation of the function.

```c
void display()
{
    printf("Hello");
}
```
