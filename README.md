# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:VAISHNAVI.S
RegisterNumber:212225230289
*/
 module Fulladder(a,b,c,sum,carry);
 input a,b,c;
 output sum,carry;
 xor(sum,a,b,c);
 assign carry=a&b | b&c | a&c;
 endmodule
 #FULL-SUBTRACTOR
 module Fullsubtractor(diff,borrow,a,b,c);
input a,b,c;
output diff,borrow;
xor(diff,a,b,c);
assign borrow= (~a)&c | (~a)&b | (b&c);
endmodule
```
**RTL Schematic**

<img width="805" height="500" alt="Screenshot 2026-03-11 202018" src="https://github.com/user-attachments/assets/fdf79caf-ebac-4369-90f5-4447f4b31d58" />

<img width="805" height="506" alt="Screenshot 2026-03-11 202130" src="https://github.com/user-attachments/assets/5ca944d2-37df-48f8-bc64-3bc38bef6b0a" />

**Output Timing Waveform**

<img width="804" height="497" alt="Screenshot 2026-03-11 202307" src="https://github.com/user-attachments/assets/e5fd9b8f-5349-48d2-94b2-ce4c891b7894" />

<img width="809" height="502" alt="Screenshot 2026-03-11 202419" src="https://github.com/user-attachments/assets/c5f7ca40-1870-4c4c-bbd8-60d27f05d3f5" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



