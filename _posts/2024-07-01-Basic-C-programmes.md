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
**The corresponding output**

```bash
To add two Numbers
Enter first Number
34
Enter second Number
67
The sum of 34 and 67 is 101.
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

**The Corresponding output**

```bash
To product three Numbers
Enter first Number
23
Enter second Number
-3
Enter third Number
12
The product of 23,-3 and 12 is -828.
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
**The corresponding output**

```bash
Test case 1:
Max of two Numbers
Enter first Number
35
Enter second Number
96
The max of 35 and 96 is 96.

Test case 2:
Max of two Numbers
Enter first Number
-98
Enter second Number
1
The max of -98 and 1 is 1

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

**The corresponding output**

```bash
Sum of Two digit number
Enter two digit number
74
sum of two digits of a number 74, is 11.

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
**The Corresponding output**

```bash
To print first 'N' naturalnumbers
Enter the 'N'
32
1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,

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
**The Corresponding output**

```bash
To print first 100 naturalnumbers
1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,

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
**The Corresponding output**

```bash
Test case 1:
To check the number is Even or Odd
Enter the Number
5674
The given number 5674 is Even.

Test case 2:
To check the number is Even or Odd
Enter the Number
3467
The given number 3467 is Odd.

```
* ### **Given a number, positive or negative**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int num;

    printf("To check the number is positive or negative\n");

    num = get_int("Enter the number\n");

    if (num >= 0)
    {
        printf("The number %i is positive.\n", num);
    }
    else
        printf("The number %i is negative.\n", num);
}
```
**The Corresponding output**

```bash
Test case 1:

To check the number is positive or negative
Enter the number
-785
The number -785 is negative.

Test case 2:

To check the number is positive or negative.
Enter the number
2356
The number 2356 is positive

```

* ### **even numbers up to `n`**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int n;
    int counter;
    printf("To print 'n' even numbers\n");

    n = get_int("Enter the number\n");
    counter = 1;
    while (counter <= n)
    {
        if ((counter % 2) == 0)
        {
            printf("%i,", counter);
        }
        counter = counter + 1;
    }
    printf("\n");
}
```
**The Corresponding output**

```bash
To print 'n' even numbers
Enter the number
22
2,4,6,8,10,12,14,16,18,20,22,

```
* ### **`n` even numbers**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int n;
    int counter;
    int even;

    printf("To print n even numbers.\n");
    n = get_int("Enter the number: ");

    counter = 1;
    while (counter <= n - 1)
    {
        even = counter * 2;
        printf("%i,", even);
        counter++;
    }
    even = counter * 2;
    printf("%i.", even);
    printf("\n");
}
```

**The corresponding output**

```bash
To print n even numbers.
Enter the number: 10
2,4,6,8,10,12,14,16,18,20.

```
* ### **Third angle of a triangle**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int angle1, angle2, sum, thirdangle;
    printf("To find the third angle of a triangle.\n");

    angle1 = get_int("Enter the first angle: ");
    angle2 = get_int("Enter the second angle: ");

    sum = angle1 + angle2;
    thirdangle = 180 - sum;

    printf("The third angle of the triangle is %i degrees.\n", thirdangle);
}
```
**The corresponding output**

```bash

To find the third angle of a triangle.
Enter the first angle: 60
Enter the second angle: 40
The third angle of the triangle is 80 degrees.

```
* ### **N Odd Numbers**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int n, counter, odd;

    printf("To display a series of odd numbers.\n");

    n = get_int("How many odd numbers would you like to see? ");

    printf("The first %i odd numbers are ", n);

    counter = 0;
    while (counter < n - 1)
    {
        odd = counter * 2 + 1;
        printf("%i, ", odd);
        counter = counter + 1;
    }
    odd = counter * 2 + 1;
    printf("%i.\n", odd);
}

```
**The corresponding output**

```bash

To display a series of odd numbers.
How many odd numbers would you like to see? 6
The first 6 odd numbers are 1, 3, 5, 7, 9, 11.

```
* ### **Odd Numbers Upto N**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int n, counter;

    printf("To display all odd numbers up to a given number.\n");

    n = get_int("Up to which number would you like to print odd numbers? ");

    printf("The odd numbers up to %i are ", n);

    counter = 0;

    while (counter < (n - 1))
    {
        if (counter % 2 != 0)
        {
            printf("%i, ", counter);
        }
        counter++;
    }

    if (counter % 2 != 0)
    {
        printf("%i.\n", counter);
    }
    if (n % 2 != 0)
    {
        printf("%i.\n", n);
    }
}

```
**The corresponding output**

```bash

To display all odd numbers up to a given number.
Up to which number would you like to print odd numbers? 10
The odd numbers up to 10 are 1, 3, 5, 7, 9.

```

* ### **Print lowercase and the corresponding uppercase letters**

```c
#include <cs50.h>
#include <stdio.h>


int main(void)
{
    char ch = get_char("Enter an lower-case letter: ");
    printf("%c --> %c\n", ch, ch- 32);

}

```
**The corresponding output**

```bash
Enter an lower-case letter: a
a --> A
```
* ### **print string ASCII codes including null**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    string str = "GO";
    printf("%i, %i, %i\n.", str[0], str[1], str[2]);
}
```
**The corresponding output**

71, 79, 0 ====> Here `71` is the ASCII code of `'G'`, `79` is the ASCII code of `'O'` and `0` is the ASCII code of `'\0'`;

