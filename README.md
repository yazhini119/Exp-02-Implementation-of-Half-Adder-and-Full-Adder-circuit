# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: YAZHINI S
RegisterNumber: 212223050062 
*/

##Code:

module YAZHINI(x,y,s,c); input x,y; output s,c; xor(s,x,y); and(c,x,y); endmodule

module full_adder(x, y, z, s, c, x1, x2, x3); input x, y,z; output s ,c, x1, x2, x3; xor(x1, x, y); xor(s, x1, z); and(x2, x, y); and(x3, x1, z); or(c, x2, x3); endmodule

### Output:
###RTL

Half adder:

![image](https://github.com/yazhini119/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155442058/ac94e647-b91d-44ce-85a5-d42c66363491)

Full adder:

![image](https://github.com/yazhini119/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155442058/2fc2e2e1-0d46-4291-ab05-094fa4aef4a3)

### TIMING DIAGRAM

Half adder:

![image](https://github.com/yazhini119/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155442058/11474d4e-ba71-4541-942f-103e7ee2f0a9)

Full adder:

![image](https://github.com/yazhini119/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155442058/48322b56-a80a-484c-9e11-3d6455d2e096)


### TRUTH TABLE 

Half adder:

![image](https://github.com/yazhini119/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155442058/13c4f389-89f6-4524-8a34-33c186de0351)

Full adder:

![image](https://github.com/yazhini119/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155442058/a1119f8f-4ecc-4b8f-8208-2ea9d19ffbb9)

### Result:Thus the half adder and full adder circuit are designed and the truth table for half adder and full adder are verified.
