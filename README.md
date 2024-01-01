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
![image](https://github.com/sandhiya2815/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155123230/ca407adf-e3aa-40b0-9877-08e00c011555)

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 

Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: saridha M A
RegisterNumber: 23013627 
*/
module project_3(sum,carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule
```
RTL realization
![image](https://github.com/sandhiya2815/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155123230/e4585857-094f-4231-9add-d610d29a6bef)
Timing diagram
![image](https://github.com/sandhiya2815/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155123230/bc76d7b7-e7a7-4880-a659-57d310b9d3f9)
Truth table
![image](https://github.com/sandhiya2815/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155123230/55bb89ab-197f-4936-981a-5c734ce44006)

Program :
```
module project_3_2(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
```
### RTL
![image](https://github.com/sandhiya2815/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155123230/4e65d33e-fc6f-44ef-9f14-35139a309d94)

### TIMING DIAGRAM
![image](https://github.com/sandhiya2815/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155123230/4c1d47a0-23a4-4d4c-b900-81f0ae8833ad)

### TRUTH TABLE 
![image](https://github.com/sandhiya2815/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155123230/fa625381-dc5b-44e9-895d-10945ac03a9b)


### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming

