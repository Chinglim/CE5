CE5
===
#Content 

Task 1: Simple MIPS Assembly Program

Task 2: Machine Code

##Task 1: Simple MIPS Assembly Program

addi $S0, $0, 44      (To initialize the register $S0 with the value 44)

addi $S1, $0, -37     (To initialize the register $S1 with the value -37)

add $S2, $S1, $S0     (To add the values within register $S1 and $S0 and then storing it into register $S2)

 SW x54, $S2          (To store the value within register $S2 now into memory address x54.
 
##Task 2: Machine Code
 
MIPS Assembly Code   

addi $S0, $0, 44 

addi $S1, $0, -37

add $S2, $S0, $S1

 SW $S2 ,x54

Machine Code (Binary)  

001000 00000 10000 0000 0000 0010 1100  

001000 00000 10001 1111 1111 1101 1011

000000 10000 10001 10010 00000 100000

101011 10010 54    0000 0000 0000 0000
 
Machine Code (Hexadecimal)

0x 2010 002C

0x 2011 FFDB

0x 0211 9020

0x 57254 0000
