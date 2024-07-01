---
title: "Basic C-programmes"
date: 2024-07-01
categories:
---

## Basic C-programmes

* ### **Sum of Two numbers**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int num1, num2, sum;
    printf("To add two Numbers\n");
    num1 = get_int("Enter first Number\n");
    num2 = get_int("Enter second Number\n");
    sum = num1 + num2;
    printf("The sum of %i and %i is %i.\n", num1, num2, sum);
}
```
* ### **Product of Three numbers**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int num1, num2, num3, product;

    printf("To product three Numbers\n");

    num1 = get_int("Enter first Number\n");
    num2 = get_int("Enter second Number\n");
    num3 = get_int("Enter third Number\n");

    product = num1 * num2 * num3;
    printf("The product of %i,%i and %i is %i.\n", num1, num2, num3, product);
}
```
* ### **Maximum of Two numbers**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int num1, num2, max;
    printf("Max of two Numbers\n");
    num1 = get_int("Enter first Number\n");
    num2 = get_int("Enter second Number\n");

    if (num1 == num2)
    {
        max = num1;
        printf("The max of %i and %i is %i.\n", num1, num2, max);
    }
    else if (num1 > num2)
    {
        max = num1;
        printf("The max of %i and %i is %i.\n", num1, num2, max);
    }
    else
    {
        max = num2;
        printf("The max of %i and %i is %i.\n", num1, num2, max);
    }
}
```
* ###  **sum of two digit numbers**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int Number, sum;

    printf("Sum of Two digit number\n");

    Number = get_int("Enter two digit number\n");
    sum = (Number % 10) + (Number / 10);

    printf("sum of two digits of a number %i, is %i.\n", Number, sum);
}
```
* ### **First N natural numbers**

```c 
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int N;
    int counter;
    printf("To print first 'N' naturalnumbers\n");

    N = get_int("Enter the 'N'\n");
    counter = 1;
    while (counter <= N)
    {

        printf("%i,", counter);

        counter = counter + 1;
    }
    printf("\n");
}
```
* ### **First 100 natural numbers**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // int N=100;
    int counter;
    printf("To print first 100 naturalnumbers\n");

    // Number = get_int("Enter the Number\n");
    counter = 1;
    while (counter <= 100)
    {

        printf("%i,", counter);

        counter = counter + 1;
    }
    printf("\n");
}
```
* ### **Given a number, odd or even**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int num;

    printf("To check the number is Even or Odd\n");

    num = get_int("Enter the Number\n");
    if ((num % 2) == 0)
    {
        printf("The given number %i is Even.\n", num);
    }
    else
    {
        printf("The given number %i is Odd.\n", num);
    }
}
```
