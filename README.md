# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
It can be implemented using two half subtractors and one OR gate as: Giving one half subtractor the inputs A and B that gives outputs Diff1 and B1. Giving second half subtractor inputs Bin and Diff1 from first subtractor that gives outputs B2 and D (difference for the full subtractor).





## Program:
```py
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:R.Kavi Keerthana 
RegisterNumber:212222100022

Half subtractor: module halfsubtractor(A,B,Difference,Borrow); input A,B; output Difference,Borrow; assign Difference = (A^B); assign Borrow = (~A&B); endmodule

Full subtractor: module fullsub(A,B,C,Difference,Borrow); input A,B,C; output Difference,Borrow; assign Difference = (A^B^C); assign Borrow = (~A&(B^C)|(B&C)); endmodule */
```

## Output:
## Logic gates:
## FULL SUBTRACTOR:
![image](https://github.com/RKavikeerthana/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120431120/bd74b2c4-7941-45e2-889c-6ddf1cce44ca)
## HALF SUBTRACTOR:
![image](https://github.com/RKavikeerthana/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120431120/4b205095-5c00-405a-a890-721367741c41)

## Truthtable
## FULL SUBTRACTOR:
![image](https://github.com/RKavikeerthana/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120431120/25c66cf8-1b70-4096-acc1-0158339416b1)

## HALF SUBTRACTOR:
![image](https://github.com/RKavikeerthana/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120431120/217c8a17-2860-496c-949a-20ba6531b114)
## RTL realization
## FULL SUBTRACTOR:
![image](https://github.com/RKavikeerthana/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120431120/31535c43-32b3-46ff-8af3-67927803b889)
## HALF SUBTRACTOR:
![image](https://github.com/RKavikeerthana/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120431120/0353f588-9a7e-48e7-b5d4-595539c4eade)
## Timing diagram
## FULL SUBTRACTOR:
![image](https://github.com/RKavikeerthana/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120431120/310f5a1c-c06f-4d56-ac8d-68c94fefa3fa)
## HALF SUBTRACTOR:
![image](https://github.com/RKavikeerthana/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120431120/ebc1b520-2af2-4b3b-affc-a64e9ad20aed)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
