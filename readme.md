# Tiny Virtual Machine

My program is intended to be used to read files(elf.txt) and print instructions depending on the output from the programs user. 
It reads the Opcodes in the file that specify an operation or instruction to be performed. 
Output prints the state of the PC, A and Memory after user input. Its structure includes functions to fetch, store, add, load, sub, input, and 
output instructions.

> what opcodes does your tiny virtual machine adhere to?
5 5
3 0
6 9
5 5
3 1
6 9
5 5
3 4
6 9
1 1
3 3
1 2
2 0
3 2
1 3
4 4
3 3
9 0
8 11
1 2
6 9
7 0


Opcode  mnemonic    meaning
01      LOAD X      A <— DM[x]
02      ADD X       A <— A + DM[x]
03	STORE X	    DM[x]<- A
04	SUB X	    A <— A - DM[x]
05	IN X	    A <— Read from Device
06	OUT X       A —> Write to device
07	END X	    End of program (stop running)
08	JMP X       PC <— x
09 	SKIPZ X     If A is equal zero, PC = PC + 2



Assignment: Programming Project 3 (Tiny Harvard Architecture ISA) HW3

Author: Aaron Gould

School: University of Central Florida

Professor:  Euripides Montagne
Class:      CGS3269
Due date:   11/28/2023

Language: C

To Compile: I used replit to compile my code. gcc main.c

To Execute: ./a.out elf.txt > output.txt 

When: Input file is named elf.txt in replit, pairs of Opcodes to read. user inputs a number and reads the list
Note: output.txt outputs the programs intentions