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