# Introduction
This is a crackme challenge made my “crackinglessons.com”. A simple GUI-based crackme which is intended for beginner reverse engineers.
The challenge:
1. Find the serial key and enter it in the textbox.
2. Patch the file to always show the congrats message when you click the Check button.

In this writeup, I created three sections for analysis. First one is for static analysis, second section is for dynamic analysis, and the last one is for disassembling and debugging. The static analysis will be the part where i’ll find the characteristics and any interesting attribute of the software. 
The dynamic analysis will be the part where i’ll run the program, find out its behaviors, what it looks like and what it will do.
And the last part is disassembling and debugging where i'll analyze the low level code of the program.

# Static Analysis
The first thing i did is to find out what are the attributes of the program and i used pestudio to determine the attributes. As per the software author, the compiler that they used is Visual studio C++ 2017. The software is GUI and it runs on a 32bit machine.
![](image/figure1.png)
