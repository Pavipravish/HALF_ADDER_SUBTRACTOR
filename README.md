# HALF_ADDER_SUBTRACTOR
# **DATE**: 15/04/2025

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

# Truth Table
![WhatsApp Image 2024-12-21 at 09 37 41_6bcda97b](https://github.com/user-attachments/assets/d51d43bb-d91e-4682-8fab-e234dff43d9b)


**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)



# Truthtable
![WhatsApp Image 2024-12-21 at 09 36 46_bad85c66](https://github.com/user-attachments/assets/9ff1687f-e02d-44be-ae00-b0559d7e801b)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
**Half_adder**
```
module halfadd_top(a,b,sum,carry);
input a,b;
output sum,carry; 
 assign sum = a^b;
 assign carry = a & b;
endmodule
```

**Half_subtractor*8
```
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
  assign Bo = ~a & b;
endmodule
```
Developed by: PRAVISH J
RegisterNumber: 24901067

**RTL Schematic**
**Half adder**
![image](https://github.com/user-attachments/assets/3c2b7b8a-74a6-447b-b24e-5b8c743fd7fd)

**Half subtractor**
![image](https://github.com/user-attachments/assets/af46461b-d3b6-4476-ab3b-debd944a298a)


**Output/TIMING Waveform**
**Half adder**
![image](https://github.com/user-attachments/assets/3b681cde-a3ed-4f33-9d39-ba106897c20f)

**Half subtractor**
![image](https://github.com/user-attachments/assets/77cb0509-b028-47b9-a833-a1de47796608)

**Result:**
The code is executed successfully
