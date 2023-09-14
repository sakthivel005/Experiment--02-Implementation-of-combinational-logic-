## Name:Sakthivel R
## Reg No:212222100044
## Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
```
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
```

## Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

1.AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

2.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation. Y= A+B


 

## Logic Diagram
## Procedure:
1.Use module projname(input,output) to start the Verilog programmming. 2.Assign inputs and outputs using the word input and output respectively. 3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression. 4.Use each output to represent one for F1 . 5.End the verilog program using keyword endmodule.


## Program:
## Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Sakthivel R
RegisterNumber:212222100044

```
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module imp(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire p,q,r,s,t;
assign p = (~A & ~B & ~C & ~D);
assign q = (A & ~C & ~D);
assign r = (~B & C & ~D);
assign s = (~A & B & C & D);
assign t = (B & ~C & D);
assign F1 = p | q | r | s | t;
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy

module imp(w,x,y,z,F2);
input w,x,y,z;
output F2;
wire p,q,r,s,t;
assign p= (x & ~y & z);
assign q= (~x & ~y & z);
assign r= (~w & x & y);
assign s= (w & ~x & y);
assign t= (w & x & y);
assign F2= p | q | r | s | t;
endmodule



```

## RTL realization
## Output:
## Logical Diagram:
![Screenshot 2023-09-14 180918](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/441a00b6-57cb-4c4c-977a-0e10ebe523d1)


## RTL realization
## For F1

![Screenshot 2023-09-14 180938](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/88797754-8b6c-4ed0-97c7-5eb42c8deb4e)

## For F2
![Screenshot 2023-09-14 180952](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/96449c16-9d39-4ec0-94bb-f4f654fe1eed)


## Timing Diagram
## For F1
![Screenshot 2023-09-14 181010](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/703bdfd0-10a6-4baa-8ef0-d39bfe90cfb7)


## For F2
![Screenshot 2023-09-14 181025](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/3d5109fa-ef52-4715-8f59-45cbe5af473a)




## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
