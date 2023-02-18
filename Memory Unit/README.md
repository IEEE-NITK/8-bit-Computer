### Memory Unit
The RAM module stores instructions along with the required addresses or required data to be operated upon. It consists of 2 submodules: the Memory Address Register(MAR) module and the actual RAM module

### Memory Address Register(MAR) Module 
This module consists of 2:1 mux (74LS157 IC), 4 bit D register(74LS173), a 4 bit dip switch, and a select toggle switch. The select toggle switch, along with the 2:1 mux is used to toggle between address incoming from the bus or address which can be entered manually using the 4 bit dip switch. 
The incoming address from the bus(BUS_0 to BUS_3) is stored into the 4 bit D Register. One set of inputs of the mux is given from the 4 bit dip switch, while the other set of inputs is given from the output of the D register. The output of the mux is decided by the select toggle switch, which can be toggled physically. This address output (A0-A3) is sent back to the bus, from where the RAM module takes it and operates on it.

### RAM Module
The RAM module consists of two 74189 ICs that can store 4 bits of data and have addresses of 4 bitlength giving a total storage capacity of 8 bytes each. They both are used in parallel to achieve a total of 8 bit RAM.
The Address input to the 74189 IC comes from the bus (A0-A3) and the data input to the RAM IC’s may come either from the bus or the dip switches. The Input is selected using a 8 bit parallel MUX, which is constructed from 74157 ICs (parallel select quad 2:1 Mux). The output of the RAM ICs is inverted using 7404 IC (Hex inverter) and given to the 74245 IC (octal bus) to be fed into the bus. The write enable is given from a 2:1 mux that selects manual enable or the enable signal given from the control line.

![image](https://user-images.githubusercontent.com/97294953/218693721-821a8e99-51b7-4956-9831-aaccbdf32edc.png)

* Schematic of MAR module:

* Schematic of RAM module

