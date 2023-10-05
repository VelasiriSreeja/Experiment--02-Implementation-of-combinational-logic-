# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 ## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime

## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

OR Gate:
The OR gate is a fundamental digital logic gate that operates on two binary inputs, producing an output of 1 if at least one input is 1. It symbolizes logical disjunction and is essential in building logical circuits and decision-making processes in computers and electronics.

AND Gate:
The AND gate is a fundamental digital logic gate with two inputs and one output. It produces a high output (1) only when both input signals are high (1). If any input is low (0), the output remains low. It's a building block for more complex logic circuits and is integral in digital computations.

NOT Gate:
The NOT gate is a fundamental digital logic gate. It has a single input and a single output. The output is the inverse of the input: if the input is high (1), the output is low (0), and vice versa. It's a basic building block in digital circuits, used for logic inversion.

## Procedure
1.Create a New Project:

Open Quartus and create a new project by selecting "File" > "New Project Wizard."

Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2.Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."

Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3.Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4.Compile the Project:

To compile the project, click on "Processing" > "Start Compilation" in the menu.

Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5.Analyze and Fix Errors:*

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.

Review and fix any issues in your code if necessary.

View the RTL diagram.

6.Verification:

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".

Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.

Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.

Program:
 
## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: v.sreeja
RegisterNumber: 212222230169 
*/
```
module p2(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;
assign x1=(~A & ~B & ~C & ~D);
assign x2=(A & ~C & ~D);
assign x3=(~B & C & ~D);
assign x4=(~A & B &C &D);
assign x5=(B & ~C &D);
assign F1=x1 | x2 | x3 | x4 | x5;
endmodule
```
## RTL realization
![Screenshot (356)](https://github.com/VelasiriSreeja/Experiment--02-Implementation-of-combinational-logic-/assets/118344328/5b2b4a29-4008-45a5-800d-f826dd9804da)

## Truth table
![Screenshot (373)](https://github.com/VelasiriSreeja/Experiment--02-Implementation-of-combinational-logic-/assets/118344328/6bc9473f-9933-498d-8ff2-b39e4d79b6c9)


## Timing Diagram
![Screenshot (374)](https://github.com/VelasiriSreeja/Experiment--02-Implementation-of-combinational-logic-/assets/118344328/eea07edb-c508-4dcb-9e21-ce8a15bd2416)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
