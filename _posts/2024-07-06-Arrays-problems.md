---
title: "Arrays Problems"
date: 2024-07-06
categories:
---

### **Practice problems based on Arrays**

```c
#include <cs50.h>
#include <stdio.h>

void print_list(int list[]);
void sumofarrayelements(int list[], int sum);

int main(void)
{
    int list[] = {10, 30, 20};
    print_list(list);
    int sum = 0;
    sumofarrayelements(list, sum);
}

void print_list(int list[])
{
    printf("Apples: %i\n", list[0]);
    printf("Bananas: %i\n", list[1]);
    printf("Mangos: %i\n", list[2]);

}
void sumofarrayelements(int list[], int sum)
{
    sum = list[0] + list[1] + list[2];
    printf("%i\n", sum);
}

```
**The Corresponding output**
```bash
Apples: 10
Bananas: 30
Mangos: 20
60

```
### **mistakes**

* Forgot to initialize the `sum` value to the `Zero`

c:12:30: error: variable 'sum' is uninitialized when used here [-Werror,-Wuninitialized]
    sumofarrayelements(list, sum);
                             ^~~
                             
arrays_practice.c:11:12: note: initialize the variable 'sum' to silence this warning
    int sum;
           ^
            = 0

* In line number 19 on this page I am giving index value i.elist[3](index out of bound for this length i.e3). Have to pass only parameter i.elist.

By "incompatible conversion", clang means that you are assigning a value to a variable of a different type on line 10 of
arrays_practice.c. Try ensuring that your value is of type pointer.            

### **Character Array introduction**

* A character array is a sequence of characters stored in contiguous memory locations.

* You can declare, initialize, and modify character Arrays.

* You can access elements in the array using indexing.

*  In C, character arrays are often used to store strings, which are sequences of characters terminated by a null character 
    `('\0')`.
    
**Declaring a Character Array**

To declare a character array, you specify the type (char), the array name, and the size of the array in square brackets.

Example: char name[10];

This declares a character array named name that can hold up to 9 characters (plus the null terminator).

**Initializing a Character Array**

You can initialize a character array at the time of declaration in two ways:

* By specifying individual characters:

char name[6] = {'H', 'e', 'l', 'l', 'o', '\0'};

* By using a string literal

char name[6] = "Hello";
In this case, the size of the array is automatically determined by the length of the string plus the null terminator.

* You can access and modify elements in a character array using array indexing

        name[0] = 'H';    name[1] = 'e';

**Practice programme**

```c

#include <cs50.h>
#include <stdio.h>


void printArrayElements(char name[6]);

int main(int argc, string words[])
{
    words[0] = "HI";
    words[1] = "BYE";
    words[3] = "HELLO";
    char name[6] = {'G','A','N','G','A','\0'};
    printArrayElements(name);

    printf("%s ", words[0]);
    printf("%s\n", words[1]);
    printf("%c%c%c%c%c\n", words[3][0], words[3][1], words[3][2], words[3][3], words[3][4]);
}
void printArrayElements(char name[6])
{
    printf("%c%c%c%c%c\n", name[0], name[1],name[2],name[3],name[4]);
}

```
**The corresponding output**

```bash
GANGA
HI BYE
HELLO

```
* **mistakes**
* Characterarray.c:7:5: error: first parameter of 'main' (argument count) must be of type 'int'

    int main(string words[],int argc)
    
* Characterarray.c:17:22: error: more '%' conversions than data arguments [-Werror,-Wformat-insufficient-args]

    printf("%c%c%c%c%c", words[3][0], words[3][1], words[3][2], words[3][3]);    

* Characterarray.c:13:29: error: expected expression

    printArrayElements(name[]);