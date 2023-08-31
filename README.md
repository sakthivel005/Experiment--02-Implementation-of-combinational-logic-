![Screenshot 2023-08-31 084722](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/b8944a10-5d47-420a-92f5-4ada77eba291)![Screenshot 2023-08-31 084722](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/15280e50-2f57-4b80-8687-67fc77f07adb)## Name:Sakthivel R
## Reg No:212222100044
# Experiment--02-Implementation-of-combinational-logic
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
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Sakthivel R
RegisterNumber:212222100044
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
module ex2(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;
assign x1 = (~A & ~B & ~C & ~D);
assign x2 = (A & ~C & ~D);
assign x3 = (~B & C & ~D);
assign x4 = (~A & B & C & D);
assign x5 = (B & ~C & D);
assign F1 = x1 | x2 | x3 | x4 | x5;
endmodule



```

## Truth Table:



![Screenshot 2023-08-31 192940](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/282b4ab1-d975-4294-bbf0-e2da7ddf4355)





## RTL realization:
![Screenshot 2023-08-25 083711](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/b10909a4-1640-42c5-8d1a-476cf91193e0)


## Output:


![Screenshot 2023-08-31 192732](https://github.com/sakthivel005/Experiment--02-Implementation-of-combinational-logic-/assets/120550359/f01c253e-5c73-4286-8c32-c2cffbc7a8db)



## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
