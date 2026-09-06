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
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:G.DHARNISH
RegisterNumber:212225040069
*/
```
module exp3(input A,B,Cin,output SUM,CARRY,BO,DIFF);
//nput A,B,Cin;
//output SUM,CARRY,BO,DIFF;
//Full adder logic
assign SUM=A^B^Cin;
assign CARRY=((A&B)|(B&Cin)|(A&Cin));
//Full Subtractor logic
assign DIFF=A^B^Cin;
assign BO=((~A&B)|(B&Cin)|(~A&Cin));
endmodule
```



**RTL Schematic**
<img width="1917" height="1001" alt="image" src="https://github.com/user-attachments/assets/f54a5182-96d8-47ce-9c9e-0eec9d739ac1" />



**Output Timing Waveform**
<img width="1917" height="1015" alt="image" src="https://github.com/user-attachments/assets/d6f277ae-37cc-47ea-897a-47e56ee82e36" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



