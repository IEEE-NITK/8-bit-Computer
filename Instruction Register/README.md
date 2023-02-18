### Instruction Register
The instruction register (IR)is very similar to the A and B registers with few differences in working and usage. The IR stores the address of the instructions in 4 bits. The 4 bits are the last four least significant bits (LSB) of the IR. These bits indicate the instruction to be executed and can be loaded to the bus using the enable pin. The remaining 4 bits which are the most significant bits (MSB) of the IR are sent to the instruction decoder.


![image](https://user-images.githubusercontent.com/97294953/218691234-b61d97b1-c89e-4693-8440-ef92a5610ca2.png)

* Schematic of Instruction Register:
https://github.com/IEEE-NITK/8-bit-Computer/blob/main/Instruction%20Register/Instruction%20Register%20Schematic.png?raw=true
