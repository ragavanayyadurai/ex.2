### Ex. No. : 2 
### Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:
![image](https://github.com/R-Udayakumar/ex.2-Combination-circuit/assets/118708024/e43d848d-9e73-423f-abba-315bb59cfe5c)

![image](https://github.com/R-Udayakumar/ex.2-Combination-circuit/assets/118708024/3b3e9941-4e20-4ff3-bada-fb7b5f874daf)

## Truth Table:
![s1](https://github.com/MOHAMEDGOWS/ex.2/assets/117954463/c58ffaab-14a0-47f8-b92a-53c66206c2fa)

## Program:
```
module exp2a(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire adash,bdash,cdash,ddash,x,y,z,p,q,r;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(x,bdash,ddash);
and(y,adash,b,d);
and(z,a,b,cdash);
or(f1,x,y,z);
and(p,cdash,d);
and(q,a,c);
and(r,b,c);
or(f2,p,q,r);
endmodule
```

## RTL Schematic:
![image](https://github.com/R-Udayakumar/ex.2-Combination-circuit/assets/118708024/1afc100d-5a62-4c21-a5fb-07d7e431ad51)

## Timing Diagram:
![image](https://github.com/R-Udayakumar/ex.2-Combination-circuit/assets/118708024/ac12ea06-92d0-4be6-b489-16a71e7f8c98)

## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.


