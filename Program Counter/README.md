### Program Counter
The program counter uses a 74161 IC, which is a 4 bit synchronous counter IC that also consists of parallel load and count enable. 
The program counter, by default starts from 0000 and increments every program cycle (not the same as every clock cycle). It generates the memory address of the next instruction to be accessed from the RAM and feeds it into the bus, (A0-A3) using the 74245 IC (octal bus). The enable pin allows the count to be incremented every program cycle. The program counter is also capable of reading a 4 bit memory address from the bus using the load enable coming from the control line. This is important for jumping to certain instructions or looping a set of instructions.

![image](https://user-images.githubusercontent.com/97294953/218692870-6b3eef5b-7dde-4229-a589-0858d6c93eb0.png)

* Schematic of Program Counter module
https://github.com/IEEE-NITK/8-bit-Computer/blob/main/Program%20Counter/Program%20Counter%20Schematic.png?raw=true
