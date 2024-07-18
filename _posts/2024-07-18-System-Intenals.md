---
title: "System Internals"
date: 2024-07-18
categories:
---
### **Understanding System Internals**

When we talk about "system internals," we're referring to the basic components and workings of a computer system, including both hardware and software. 

### **Hardware Components**

![Old Computer Diagram ](https://www.kindpng.com/picc/m/154-1549386_old-computer-diagram-wiring-diagram-g11-computer-components.png) 

1. **Central Processing Unit (CPU)**

    It performs mathematical and logical operations and runs programs.

2. **Memory (RAM)**

    Random Access Memory (RAM) is temporary storage that holds data and instructions the CPU is currently using. It clears when the computer is turned off.

3. **Storage (HDD/SSD)**

    * Hard Disk Drive (HDD): Uses spinning disks to store data. It's like a library with physical books.

    * Solid State Drive (SSD): Uses flash memory and is faster than HDDs. It's like an electronic library.

4. **Motherboard**

    The motherboard is the main circuit board that connects all the components. It has slots for the CPU, RAM, storage devices, and other parts.      

5. **Peripheral Devices**

    These are the external devices you use with your computer, like the keyboard, mouse, monitor, printer, and network interfaces.

### **Operating System (OS)**

The operating system is the software that manages all the hardware and provides services for running applications. 
It acts as an intermediary between users and the computer hardware.

* Managing input and output operations.

* Keeping track of where data is stored in RAM.

* Managing how data is stored and retrieved from storage devices.

* To communicate with hardware devices.

**Examples of Popular Operating Systems**

* Windows: Developed by Microsoft, widely used on personal computers.

* macOS: Developed by Apple, used on Mac computers.

* Linux: An open-source OS used on servers and desktops.

* Android: Based on Linux, used on mobile devices.

* iOS: Developed by Apple, used on iPhones and iPads.

**Summery**

The OS is essential for managing the hardware and software resources of a computer. It provides a user interface, manages processes and memory, handles file systems, and controls hardware devices. Understanding these basic points about the OS helps in grasping how computers work and how to interact with them effectively.

**Example: A Simple System Program**

Here’s a simple C program that demonstrates process creation and communication

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int num1;
    int num2;
    int sum;
    printf("To add two numbers.\n");

    printf("Enter the first number: ");
    scanf("%i", &num1);

    printf("Enter the second number: ");
    scanf("%i", &num2);

    sum = num1 + num2;

    printf("The sum of %i and %i is %i.\n", num1, num2, sum);
}

```
In this program

* **Memory Allocation for Variables:**

When the program starts, memory is allocated in the RAM for the variables num1, num2, and sum. These are integer variables, so each one typically takes up 4 bytes of memory on a 32-bit or 64-bit system.

* **Using printf and scanf Functions:**

The printf function is used to display messages to the user. It writes the specified message to the standard output (usually the screen).

The scanf function is used to read input from the user. It takes the input from the standard input (usually the keyboard) and stores it in the specified memory addresses of num1 and num2.

* **Role of the OS in printf and scanf:**

The OS facilitates the printf and scanf functions by providing access to standard input and output. It ensures that the input from the keyboard is captured and sent to the program and that the output from the program is displayed on the screen.

* **CPU Operations:**

The CPU performs the addition operation. It retrieves the values of num1 and num2 from RAM, performs the addition, and stores the result in the variable sum.

* **Storing the Computed Value:**

The computed value (sum of num1 and num2) is stored back in the RAM in the memory allocated for the variable sum.

* **Output Display:**

The printf function is called again to display the result. The OS ensures that the value of sum is correctly read from RAM and displayed on the screen.

### **The stages involve in C-program running**

![Image](https://media.geeksforgeeks.org/wp-content/uploads/123-6.png)

* write your C code in a text file with a .c extension.

* The C compiler translates the high-level C code into machine code. 

  1. The preprocessor handles directives such as #include and #define. It processes these directives and generates an expanded    source code file.

  2. The compiler translates the preprocessed code into assembly code for a specific architecture.

  3. The assembler translates the assembly code into machine code (binary code). This generates an object file (.o or .obj).
   
  4. The linker combines object files and libraries into a single executable file. It resolves references to external functions and variables.

* The operating system loads the executable file into memory and starts execution. 