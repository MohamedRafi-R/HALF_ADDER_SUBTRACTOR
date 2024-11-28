# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

![389960927-1e369af5-5a8f-46b9-a59a-2c67d7a5bde8](https://github.com/user-attachments/assets/de306b48-bcac-4193-872c-c8bb0b348f33)

![389961011-fd1b4b29-5f51-4267-a9a4-952661b7b2be](https://github.com/user-attachments/assets/8714cd92-df84-4e47-b9f0-bbe820313c7e)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
Half Adder
module exp3(sum, carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule

Half Subtractor
module exp3(diff,carry,a,b);
input a,b;
output diff,carry;
xor(diff,a,b);
assign carry=(~a)&b;
endmodule


/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: RegisterNumber:*/

**RTL Schematic**

![389961097-7f256183-54cd-4853-be1e-fee9917187f4](https://github.com/user-attachments/assets/6d1282e3-013a-4e3f-ad41-8312c77a3b45)

![389961345-61df3446-740f-4d20-bf82-0f97a2b5685c](https://github.com/user-attachments/assets/9df4f1c2-4e3a-492f-8068-77369b3ce276)

**Output/TIMING Waveform**

![389961620-355fa850-010d-4e2b-a5ad-bdd0bae02ee4](https://github.com/user-attachments/assets/caa8d1e6-8292-4b9b-ab65-1896c5d8f6a2)

![389961845-7cada583-8d2a-4e8a-a111-642aea54c83e](https://github.com/user-attachments/assets/6eff6ada-1866-4a77-b28c-19581b255753)


**Result:**
Thus the half subtractor and half adder circuits are designed and the truth tables is verified using quartus software.
