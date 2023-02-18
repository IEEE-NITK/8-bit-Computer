### Registers
The registers in a computer are data storage elements used by the CPU. Registers store small amounts of data that the CPU is processing. It usually holds the operands or the instructions that the CPU is currently processing. The 8 bit computer has 3 registers: register A register B and instruction register (IR). Registers A and B are general purpose registers used to store operands (data) or memory pointers (addresses). 

#### Register A and Register B
The A and B registers are composed of two 4 bit data registers namely 74LS173 and one 74LS245 octal bus. The two 4 bit data registers are driven by the clock module and each receive 4 data bits. The data can be transferred to the octal bus or just stored in the register based on the control pins 1 and 2 (Oe1 and Oe2, which is zero/grounded in our case). The pins 8 and 9 are load pins which are used to control loading of data from input pins to the register, when the load pin is low it loads data into the register and doesn't load when it is high. The output pins of the register are connected to LED’s to show the data stored in it and also connected to the octal bus. The bus has a direction input pin to control the direction of data flow (high, input to output pin flow in our case) and it has an enable pin which transfers data from register to bus when low and  doesn’t transfer when high.


![image](https://user-images.githubusercontent.com/97294953/218690584-5a53af80-d211-40ba-8e6f-f15545112047.png)

* Schematic of Register A:
https://github.com/IEEE-NITK/8-bit-Computer/blob/main/Register%20A/Register%20A%20Schematic.png?raw=true
* Schematic of Register B: 
https://github.com/IEEE-NITK/8-bit-Computer/blob/main/Register%20B/Register%20B%20Schematic.png?raw=true
