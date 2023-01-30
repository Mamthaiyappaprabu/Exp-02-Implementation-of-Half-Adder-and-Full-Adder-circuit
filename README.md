# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

## Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Figure -02 FULL ADDER 

## Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Mamtha.I
RegisterNumber:  22008484
*/
## Half Adder:
```
module halfadd(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
## Full Adder:
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
### Output:
### Logic symbol & Truthtable
## Half Adder:
![P3](https://user-images.githubusercontent.com/119393563/215380734-26dc8ef6-cfad-45eb-85c1-4d895e609c58.png)
<br>

## Full Adder:
![p4](https://user-images.githubusercontent.com/119393563/215380758-4c49382f-389f-4da8-be4f-bbaa4431f45b.png)
<br>

### RTL realization
## Half Adder:
![p5](https://user-images.githubusercontent.com/119393563/215380799-a3bc133c-1b34-4625-9410-f0484e7cd95d.png)
<br>

## Full Adder:
![p6](https://user-images.githubusercontent.com/119393563/215380820-5d60f278-1c0b-4faa-861e-375fa4143f94.png)
<br>

### TIMING DIAGRAM
## Half Adder:
![p7](https://user-images.githubusercontent.com/119393563/215380850-293130ab-9fae-4f11-99ee-0069ef9a30ce.png)
<br>

## Full Adder:
![p8](https://user-images.githubusercontent.com/119393563/215380880-f14f83b0-b9d4-436d-8632-079a36b8f1c3.png)
<br>


### TRUTH TABLE 
## Half Adder:
![p9](https://user-images.githubusercontent.com/119393563/215380970-bb47c93b-329b-4586-b587-6f03692cf37d.png)
<br>

## Full Adder:
![p10](https://user-images.githubusercontent.com/119393563/215381008-fc0ad107-2cde-46b4-a466-d0377ed89172.png)
<br>

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
