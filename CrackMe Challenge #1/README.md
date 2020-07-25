# Introduction
This is a crackme challenge made my “crackinglessons.com”. A simple GUI-based crackme which is intended for beginner reverse engineers.
The challenge:
1. Find the serial key and enter it in the textbox.
2. Patch the file to always show the congrats message when you click the Check button.

In this writeup, I created three sections for analysis. First one is for static analysis, second section is for dynamic analysis, and the last one is for disassembling and debugging. The static analysis will be the part where i will find the characteristics and any interesting attribute of the software. 
The dynamic analysis will be the part where i run the program, find out its behaviors, what it looks like and what it will do.
And the last part is disassembling and debugging where i analyze the low level code of the program.

# Static Analysis
The first thing i did is to find out what are the attributes of the program and i used pestudio to determine the attributes. As per the software author, the compiler that they used is Visual studio C++ 2017. The software is GUI and it runs on a 32bit machine.

![](images/figure1.png)

Next is finding useful strings in the program. I found a string “cr4ckingL3ssons” as a likely serial key to be used in the program and next to it are words like “Congrats” and “Well done!”.

![](images/figure2.png)

# Dynamic Analysis
I run the program so i could find out what it looks like and it’s behavior. The program itself have a very simple design, a window will be shown with a text box to enter the password and two buttons below.

![](images/figure3.png)

I randomly put different things to find out the behavior of the software. First, i clicked the “check” button to see what will happen.

![](images/figure4.png)

The program produced another window that says “Wrong serial key. Try again”. I tried putting a series of strings. First, i put a series of numeric number.

![](images/figure5.png)

I tried putting strings and alphanumeric but it also produces similar results. Next i used, the string “cr4ckingL3ssons” that i found earlier to test whether it will work.

![](images/figure6.png)

The program produced a different windows. I can conclude the first challenge, in which i found the serial key. Next is to disassemble the program and find where the main code and logic of the program is.

# Disassembling and Debugging
