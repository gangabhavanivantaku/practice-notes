---
title: "Scanf Function"
date: 2024-07-12
categories:
---
### **Introduction to `Scanf();` function**

In C programming, a scanner is often referred to as a function or a set of functions used to read input from the user or from files. The most commonly used function for this purpose is scanf. Here’s a basic introduction to using scanf for beginners:

### scanf Function

The scanf function is used to read formatted input from the standard input (usually the keyboard). It is part of the standard input-output library in C, so you need to include the stdio.h header file in your program to use it.

### Example: **Reading inputs and computing the sum**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int number1;
    int number2;
    float number3;
    char c;

    printf("Enter two integers, a floating-point number, and a character:\n");
    // Read the inputs
    scanf("%i %i %f %c", &number1, &number2, &number3, &c);

    int sum = number1 + number2;
    // To display the numbers and character
    printf("The entered numbers are: %i,%i,%.2f\n", number1, number2, number3);
    printf("The entered character is %c\n", c);
    // To print the sum of two numbers
    printf("The sum of Two integers is %i.\n", sum);
}
```
**The corresponding output**

```bash
Enter two integers, a floating-point number, and a character:
3 5 6.89 G
The entered numbers are: 3,5,6.89
The entered character is G
The sum of Two integers is 8.
```