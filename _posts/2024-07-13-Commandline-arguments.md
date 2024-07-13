---
title: "Commandline Arguments"
date: 2024-07-13
categories:
---
### **Print string characters by command line input**

```c
#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(int argc, string words[])
{
    int n, i;
    if (argc != 2)
    {
        printf("please provide one argument only.\n");
        return 0;
    }
    // single argument
    n = strlen(words[1]);
    printf("You have given '%s' as argument.\n", words[1]);
    printf("The individual characters are:\n");
    printf("{");
    for (i = 0; i < n - 1; i++)
    {
        printf("'%c', ", words[1][i]);
    }
    printf("'%c'}\n", words[1][n - 1]);
    return 0;
}
```
**Executes the Program in the terminal**

<script src="https://asciinema.org/a/X6oO31t7TNqP6X2N6C6NZpg0o.js" id="asciicast-X6oO31t7TNqP6X2N6C6NZpg0o" async="true"></script>

### **Print command line arguments**

```c
#include <cs50.h>
#include <stdio.h>

int main(int argc, string words[])
{

    printf("You have given %i arguments and they are:\n", argc-1);

    for(int i = 1;i < argc;i++)
    {
        printf("%i. ", i);
        printf("%s\n", words[i]);
    }
}
```
**let us see how to execute the program in the terminal**

<script src="https://asciinema.org/a/g97zhnepip31WKIiYAaMKwnHu.js" id="asciicast-g97zhnepip31WKIiYAaMKwnHu" async="true"></script>