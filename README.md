## REGISTER NUMBER:212223040212
## NAME:SUJITHRA.K
## FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

## AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Full Adder and Full Subtractor

## Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

## Figure -1 FULL ADDER

## Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## Truthtable
## FULL ADDER:
![319876844-028cafb2-6579-465e-9bbe-fe45246f3672](https://github.com/Suji-90/FULL_ADDER_SUBTRACTOR/assets/150884148/af7159f5-9486-425d-a3d8-cfce9cd84a78)

## FULL SUBTRACTOR:
![319876962-4dd6f32b-75c5-4999-bc6f-6c948efa2933](https://github.com/Suji-90/FULL_ADDER_SUBTRACTOR/assets/150884148/71fd1177-945e-45be-a824-fa5c9f057fec)

## Procedure
1)Create a New Project: *Open Quartus and create a new project by selecting "File" > "New Project Wizard." *Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2)Create a New Design File: *Once the project is created, right-click on the project name in the Project Navigator and select "Add New File." *Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3)Write the Combinational Logic Code: *Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4)Compile the Project: *To compile the project, click on "Processing" > "Start Compilation" in the menu. *Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5)Analyze and Fix Errors: *If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window. *Review and fix any issues in your code if necessary. *View the RTL diagram.

6)Verification: *Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF". *Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All. *Give the Input Combinations according to the Truth Table and then simulate the Output Waveform.


## Program:

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

## Full Adder
```
module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule
```
## Full Subtractor
```
module fullsub(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
## RTL Schematic

## Full Adder:

![318210459-fbb0551a-202f-4aae-a0de-d22f24506755](https://github.com/Suji-90/FULL_ADDER_SUBTRACTOR/assets/150884148/6b5ca9eb-a364-4365-94ad-9acb7b4da922)

## Full Subtractor
![318210531-522a1f25-8b70-4139-bd45-47f235d74331](https://github.com/Suji-90/FULL_ADDER_SUBTRACTOR/assets/150884148/97efa979-764c-410b-b5cf-78b4f8f24300)

## Output Timing Waveform

## Full Adder
![318210582-4a30573e-0766-4f04-8596-c4718b5d8241](https://github.com/Suji-90/FULL_ADDER_SUBTRACTOR/assets/150884148/4d20f705-f627-4fda-8bba-09c8dc5d250c)

## Full Subtractor
![318210618-9f1e8407-b18d-4ba7-a52f-9c653098bc7a](https://github.com/Suji-90/FULL_ADDER_SUBTRACTOR/assets/150884148/b56b036e-8720-4b77-9e47-27fd68efeda6)

## Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



