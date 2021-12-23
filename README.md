# BinaryBomblab

Defusing a Binary Bomb
The binary bomb is a program that consists of a sequence of phases. Each phase expects us to type a particular string on stdin. If we type the correct string, then the phase is defused and the bomb proceeds to next phase. On the other hand, if we provide the incorrect string bomb explodes by printing “BOOM!!!” and then terminates. The bomb has to be defused in order to proceed to next phase. 

Step 1: Getting the Bomb
README: identifies the bomb and its owners.
bomb: The executable binary bomb.
bomb.c: Source file with the bomb’s main routine and a friendly greeting from Dr.Evil.
writeup.pdf: The lab writeup

Step 2: Defuse the Bomb
We can use many tools to help defuse the bomb. The best way is to use any favorite debugger to step through the disassembled binary.
Each time my bomb explodes, it will notify the bomblab server and I will lose ½ points (up to a max of 20 points) in the final score for the lab. The first four phases are worth 10 points each while phases 6 and 7 are worth 15 points as they will be little more difficult. So the maximum score will be 70 points.
The bomb ignores input lines. We do not have to retype the solutions to phases we have already defused. (Ex. Run bomb with command line argument, ./bomb answers.txt

To avoid accidentally exploding the bomb, we can learn to single-step through the assembly code and how to set breakpoints. We will also need to learn how to inspect both the registers and the memory states. 

Tools for analyzing the bomb:
1.	gdb: GNU debugger, a command line debugger tool. Trace through a program line by line, examine memory and registers, look at both source code and assembly code, set breakpoints, set memory watch points and write scripts. Some other tips for using gdb, to keep bomb from blowing up every time wrong input is typed by setting up breakpoints and has help and man gdb.

2.	objdump –t : prints bomb’s symbol table.
3.	objdump –d: disassemble all of the code in bomb.
4.	strings: display the printable strings in the bomb.
