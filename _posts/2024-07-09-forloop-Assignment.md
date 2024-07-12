---
title: "forloop Assignment"
date: 2024-07-09
categories:
---
### **`for`loop introduction**

**Question1**

Give an introduction to a beginner about for loop?

**Answer**

A for loop is a control flow statement in programming that allows code to be executed repeatedly. It's commonly used when you know how many times you want to repeat a block of code.

The structure of a for loop in C is as follows:

```c
for (initialization; condition; increment/decrement) {  
    // code to be executed  
} 
``` 

**Initialization:** This is where you initialize your loop counter. It's executed once when the loop starts.

**Condition:** This is a boolean expression that is checked before each iteration of the loop. If it's true, the loop continues; if it's false, the loop ends.

**Increment/Decrement:** This updates the loop counter, typically increasing or decreasing its value.


For example, if you wanted to print the numbers 1 to 5, you could use a for loop like this:

```c
for (int i = 1; i <= 5; i++) {  
    printf("%d\n", i);  
}  
```
This loop starts with i equal to 1, and for each iteration, it checks if i is less than or equal to 5. If it is, it prints i and then increases i by 1. When i is no longer less than or equal to 5, the loop ends.

**Question2**

What is the most use case of for loop and what is the difference between whileloop and forloop

**Answer**

for loops are commonly used when you know the exact number of times you want to iterate over a block of code. For example, iterating over an array, where you know the length, or repeating a task a specific number of times.

The difference between a for loop and a while loop lies in their structure and use cases:

* A for loop is typically used when the number of iterations is known ahead of time. It has a built-in structure for initialization, condition checking, and incrementing/decrementing.

* A while loop is typically used when the number of iterations is not known and depends on a certain condition being met. The loop will continue as long as the condition remains true.

In essence, you can use a for loop when you know how many times you want to loop, and a while loop when you want to loop until a certain condition changes. However, both types of loops can be used interchangeably with some modifications to the code

**Youtube link to understand `for loop`**

<iframe width="560" height="315" src="https://www.youtube.com/embed/WDJpZhU-Ikc?si=tmSoYcOBd49elq3L" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### **Here is an example of `for loop` that prints the number from 1 to 10**

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int i;
    for(i = 1;i < 10; i++)
    {
        printf("%i, ", i);
    }

    printf("%i.\n", i);
}
```
**The corresponding output**
```bash
1, 2, 3, 4, 5, 6, 7, 8, 9, 10.
```

### Here is the debugging video
  

<iframe width="560" height="315" src="https://www.youtube.com/embed/4luOwft-Vms?si=5Xd0g7r5XsuyIM9-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### **This is an article on the for loop**

**Article1** [https://www.w3schools.com/c/c_for_loop.php](https://www.w3schools.com/c/c_for_loop.php)

**Article2** [See the full article](https://www.geeksforgeeks.org/for-loop-in-programming/)