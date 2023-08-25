# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 

## Logic Diagram
## Procedure
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

## Timing Diagram

## Output:
## RTL
![Screenshot (353)](https://github.com/VelasiriSreeja/Experiment--02-Implementation-of-combinational-logic-/assets/118344328/53303706-66c9-4853-865e-b9aa1e5bc341)

## Timing Diagram

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
