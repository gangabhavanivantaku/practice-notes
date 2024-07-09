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

//declaration of function
void printthreetimes(string str);

int main(void)
{
    //calling a function
    printthreetimes("Hello World");
}
    //define a function
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

### **Implement `print_next_three();`function**


```c

#include <cs50.h>
#include <stdio.h>

//declaration of a function
void print_next_three(int n);

int main(void)
{
    //function calling
    print_next_three(5);
    //again function calling with argument changing
    print_next_three(10);
}
//define a function
void print_next_three(int n)
{
    printf("%i, ", n);
    printf("%i, ", n + 1);
    printf("%i.\n", n + 2);
}

```
**The corresponding output**

```bash

5, 6, 7.
10, 11, 12.

```
**Did  mistakes**

1.**first mistake**

**While compilation:**
error: incompatible pointer to integer conversion passing 'char[2]' to parameter of type 'int' [-Werror,-Wint-conversion]
printthreetimes("5");

**By using help50:**
By "incompatible conversion", clang means that you are assigning a value to a variable of a different type on line 8 of
print3times.c. Try ensuring that your value is of type integer.

2.**second mistake**

function-practice.c:5:6: error: variable has incomplete type 'void'
void print-next-three(int n);

help50 suggestion:
Not quite sure how to help, but focus your attention on line 5 of function-practice.c!

### **Implement printevenorodd(); function**

```c
#include <cs50.h>
#include <stdio.h>

void printevenorodd(int n);

int main(void)
{
    printevenorodd(6);
    printevenorodd(15);
}
void printevenorodd(int n)
{
    if(n % 2 == 0){
        printf("The given number %i is even number.\n", n);
    }
    else
    {
        printf("The given number %i is odd number.\n", n);
    }
}

```
**The corresponding output**

```bash
The given number 6 is even number.
The given number 15 is odd number.

```
**Lets create a userdefined function with return type `int`**

#### implement string length method

```c

#include <cs50.h>
#include <stdio.h>

int string_length(string str);
int main(void)
{
    string str;
    str = get_string("Enter a string\n");
    int length = string_length(str);
    printf("%i\n", length);
}
int string_length(string str)        // int is a return type.
{                                    // string_length is function name
    int n = 0;                       // string is a parameter type
    while(str[n] != '\0')            // str is a parameter
    {                                // Ganga Bhavani is arugument.
        n++;
    }
    return n;
}

```
* **outut**:   13.
  

### Note

**There is an inbuilt function or predefined function in C-library.**

#### strlen(parameter);

This function is in `<string.h>` header file.

* The corresponding code

```c
#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    string name = "Ganga Bhavani";
    /*int n = 0;
    while(name[n] != '\0')
    {
        n++;
    }*/
   int length = strlen(name);
    printf("%i\n", length);
}

```

* outpout: 13.