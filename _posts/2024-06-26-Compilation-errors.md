---
title: "Compilation errors"
date: 2024-06-26
categories:
---
## C-Code errors
### Compilation errors
 **hello.c file**
```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    string name
    name = getstring("What's your name? ");
    printf("Hello, %s\n");
}
```
### First Error :   Missing  `_`  in **get_string()** method.
```bash
  hello.c:7:12: error: implicit declaration of function 'getstring' is invalid in C99
```
### Second Error :  Forgot to give  _**variablename**_  in  _**printf()**_  function. 
Find the error with the help of **`help50`**
```bash
 You have too many format codes in your format string on line 8 of hello.c. Be sure that the number of
format codes equals the number of additional arguments.
```
### Third Error  :  Missing  `;` at variable declaration.
```bash
hello.c:6:16: error: expected ';' at end of declaration
```
_**These are the three mistakes i made in the above C-code**_

