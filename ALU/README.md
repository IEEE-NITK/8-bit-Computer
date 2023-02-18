### ALU
The alu in this 8 bit computer performs basic arithmetic like addition and subtraction on 8 bit binary numbers. To perform this, two 4 bit adders have been used (IC 74LS283). The 1st operand(A0-A7) goes directly to each 4 bit adder (1st 4 bits to the 1st adder and the last 4 bits to the other adder). Since the subtraction is of 2s complement form, each bit of the second operand(B0-B7) is 1st fed into one of the inputs of 8 XOR gates(IC 74LS86), and the second input of the 8 XOR gates is a common subtract enable signal. Whenever this subtract enable signal is off, addition takes place between the 2 operands and whenever this signal is on, subtraction takes place between the 2 operands(1st operand - 2nd operand). The output of the 8 XOR gates is the original number whenever the subtract enable signal is off, and the 1s complement form of the 2nd operand whenever the subtract signal is turned on. And this result is fed into the two 4 bit adders in a similar fashion as the 1st operand.

Since the subtraction is 2s complement, the subtract enable signal is itself fed as the carry in of the 1st adder, and the carry out of the 1st 4 bit adder is sent as the carry input to the 2nd 4 bit adder. Note that the resultant number is also of the 2s complement form. 

The resultant number at the output(BUS_0-BUS_7) of the 4 bit adders is sent to the octal bus(74LS245) and is displayed using LEDs at the each output pin of the two 4 bit adders. 

![image](https://user-images.githubusercontent.com/97294953/218692153-dc765765-47df-4c85-b71f-2756b2bb3c95.png)

* Schematic of ALU module:
