CE5
===
#Content 

Task 1: Simple MIPS Assembly Program

Task 2: Machine Code

##Task 1: Simple MIPS Assembly Program

addi $S0, $0, 44      (To initialize the register $S0 with the value 44)

addi $S1, $0, -37     (To initialize the register $S1 with the value -37)

add $S2, $S1, $S0     (To add the values within register $S1 and $S0 and then storing it into register $S2)

 SW $S2, x54($0)       (To store the value within register $S2 now into memory address x54.
 
##Task 2: Machine Code
 
MIPS Assembly Code   

addi $S0, $0, 44 

addi $S1, $0, -37

add $S2, $S0, $S1

 SW $S2 ,0x54($0)    

Machine Code (Binary)  

001000 00000 10000 0000 0000 0010 1100  

001000 00000 10001 1111 1111 1101 1011

000000 10000 10001 10010 00000 100000

101011 00000 10010 0000 0000 0011 0110
 
Machine Code (Hexadecimal)

0x 2010 002C

0x 2011 FFDB

0x 0211 9020

0x AC12 0036

Explanation of screenshot waveform

As based on the textbook pg 300 Table 6.1-MIPS register set and the task2 waveform diagram posted, 

The number for registers $S0=16 , $S1=17 and $S2=18 respectively. 

Based on the instruction on the lab sheet, one is supposed to place the decimal value 44 into $S0 and decimal value -37 into $S1 and then sum these 2 values up and place their result into register $S2.

This is correctly verified by the posted task2 image waveform which show the decimal value 44 in register 16, decimal value -37 in register 17 and decimal value 7, which is the result of 44-37, in register 18.

Therefore, i will conclude that the program is working.

## Task 3: Adding ori instruction

The necessary changes are as depicted in the diagrams attached in this repo. They are the MIPS processor schematic, the main decoder table and ALU decoder table. 

Minor changes has to be done to the codes in order to allow for the ori instruction to be implemented.

Firstly, the instruction : instr <= x"36538000";
                  wait for clk_period;   
has to be placed on the testbench.vhd for the ori insrtuction to be carried out. 

Second,  an additional instruction: when "001101" => controls <= "1010000011"; -- ori has to be added to the architecture code of the main decoder so that the new operation can be carried out and the respective individual signals to the respective components can be successful. Analysis of the code was thru analysis of using the textbook and also with the consultation of Cpt Sliva.
                  
                  
