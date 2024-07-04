---
title: "Create a Functions"
date: 2024-07-04
categories:
---

### **Implement `printthreetimes();` function**

### **For string input**

```c

#include <cs50.h>
#include <stdio.h>

void printthreetimes(string str);

int main(void)
{
    printthreetimes("Hello World");
}

void printthreetimes(string str)
{
    printf("%s\n", str);
    printf("%s\n", str);
    printf("%s\n", str);
}
```
**The corresponding output**

```bash

Hello World
Hello World
Hello World

```
* **Did One Mistake** 

You seem to be using string on line 3 of print3times.c as though it's a type, even though it's not been defined
as one. Did you forget #include <cs50.h> atop print3times.c?

### **Implement printthreetimes():function**

### **For int input**

```c

#include <cs50.h>
#include <stdio.h>

void printthreetimes(int n);

int main(void)
{
    printthreetimes(5);
    printthreetimes(10);
}

void printthreetimes(int n)
{
    printf("%i, ", n);
    printf("%i, ", n * 2);
    printf("%i.\n", n + 2);
}

```
**The corresponding output**

```bash

5, 10, 7.
10, 20, 12.

```
**Did one mistake**

**While compilation:**
error: incompatible pointer to integer conversion passing 'char[2]' to parameter of type 'int' [-Werror,-Wint-conversion]
printthreetimes("5");

**By using help50:**
By "incompatible conversion", clang means that you are assigning a value to a variable of a different type on line 8 of
print3times.c. Try ensuring that your value is of type integer.