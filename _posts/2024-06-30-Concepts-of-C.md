---
title: "Concepts of `C`"
date: 2024-06-30
categories:
---

## Fundamental Concepts of `C-language`

 * ### **C-pragramme vocabulary**
    Here's a glossary of essential vocabulary used in C programming:

    * **Variable**: A storage location identified by a name, `used to hold data`.

    * **Constant**: A value that does not change during the execution of a program. Declared using the `const` keyword.

    * **Data Type**: Defines the type of data a variable can hold, such as `int`, `float`, `char`, and `double`.

    * **Function**: A block of code that `performs a specific task`, defined using the return_type function_name(parameters)
       syntax.

    * **Loop**: A control structure that repeats a block of code multiple times. Types include `for`, `while`, and `do-while`.

    * **Conditional Statement**: A control structure that executes a block of code based on a condition. Includes `if`, 
        `else if`, and `else`.

    * **Keyword**: Reserved words with special meaning in C, such as `return`, `static`, `extern`, `break`, and `continue`.

    * **Header File**: A file containing declarations for functions and macros, included in a program using the `#include` 
         directive.

    * **Compilation**: The process of converting `source code` into `executable code`.

    * **Memory Allocation**: The process of `reserving memory` for `variables` or `data structures`. Can be static (compile-time)

        or dynamic (runtime) using functions like malloc and free.

    * **Recursion**: A programming technique where a `function calls itself`.

    * **Null Pointer**: A special pointer value indicating that it points to `no valid memory location`, usually defined as NULL.

     Understanding these terms is crucial for mastering C programming and effectively writing and debugging C code.


 * ### **Basic datatypes**

    #### Data types specify the type of data that can be stored in a variable. Examples include:

    1. **int**: Used to store _**integers**_.

     Example: `int a = 5`;

    2. **float**: Used to store _**floating-point numbers**_ (single precision).

     Example: `float b = 3.14`;

    3. **double**: Used to store _**double-precision floating-point numbers**_.

     Example: `double c = 3.14159265359`;

    4. **char**: Used to store single _**characters**_.

     Example: `char d = 'A'`;


 * ### **Keywords**
   #### Keywords are reserved words that have special meaning in the C language. They cannot be used as identifiers (variable names, function names, etc.). 

    1. **if, else** (conditional statements)

    2. **for, while** (loops)

    3. **return** (return a value from a function)

    4. **const** (constant variable)

    5. **static, extern** (storage class specifiers)

    
 * ### **C-Algorithm Steps**

  1. **Start**
  2. **Input**
  3. **Process**
  4. **Output**
  5. **End**


   **_Corresponding C-code_**

```c
//header
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    //varible declaration
    int num1, num2, sum;
    //content
    printf("To add two Numbers\n");
    //input from keyboard
    num1 = get_int("Enter first Number\n");
    num2 = get_int("Enter second Number\n");
    //compute
    sum = num1 + num2;
    //Output
    printf("The sum of %i and %i is %i.\n", num1, num2, sum);
}
```

