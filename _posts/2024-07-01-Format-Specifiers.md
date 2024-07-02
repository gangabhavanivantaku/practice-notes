---
title: "Format Specifiers"
date: 2024-07-01
categories:
---

### **_Format Specifiers_**

Different format specifiers are listed below

* `%d` or `%i`  ----> for decimal integer.
* `%f` and `%.2f` ----> for floating point.

    `%f` gives 6 decimal floating points.

    `%.2f` gives 2 decimal floating points.
* `%c` ----> Single character.

* `%s` ----> String of characters.

### **_Example Usage_**
```c
#include <cs50.h>
#include <stdio.h>

int main(void){
    int num = 10;
    float fnum = 20.8673;
    char c = 'a';
    string name = get_string("My name is\n");
    //decimal integer
    printf("%i\n", num);
    //gives 6 decimal floating points
    printf("%f\n", fnum);
    //gives 2 decimal floating points
    printf("%.2f\n", fnum);
    //gives character
    printf("%c\n", 'a');
    //gives string
    printf("%s\n", name);

}
```
**_This code will give output_**

```bash
My name is
Ganga
10
20.867300
20.87
a
Ganga
```