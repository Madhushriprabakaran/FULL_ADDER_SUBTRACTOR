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
Full Adder
Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin
Carry = AB + ACin + BCin
![image](https://github.com/user-attachments/assets/8c40590e-ecaa-4c64-8778-0b0d5685d26f)

Full Subtractor
Diff = A ⊕ B ⊕ Bin
Borrow out = A'Bin + A'B + BBin
![image](https://github.com/user-attachments/assets/189c428f-3ee9-446e-b5ee-8e6f398bc440)

**Procedure**
1.Write the detailed procedure here
2.type the program in Quartus software.
3.Compile and run the program.
4.Generate the RTL schematic and save the logic diagram.
5.Create nodes for inputs and outputs to generate the timin diagram.
6.For different input combinations generaye the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
Full Adder
Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin
Carry = AB + ACin + BCin
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

FULL SUBTRACTOR
Diff = A ⊕ B ⊕ Bin
Borrow out = A'Bin + A'B + BBin
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```

Developed by:P.Madhushri

RegisterNumber:24005365
*/
**RTL**
Full Adder
Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin
Carry = AB + ACin + BCin
![image](https://github.com/user-attachments/assets/51c687a5-ad6c-4771-8a5d-31d4a8ee45c2)
FULL SUBTRACTOR
Diff = A ⊕ B ⊕ Bin
Borrow out = A'Bin + A'B + BBin
![image](https://github.com/user-attachments/assets/bb904035-6377-4f14-86a8-c50bf43f474c)

**Output**
Full Adder
Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin
Carry = AB + ACin + BCin
![image](https://github.com/user-attachments/assets/e74c4f93-898a-4b8a-bb44-3840778bdebc)

FULL SUBTRACTOR
Diff = A ⊕ B ⊕ Bin
Borrow out = A'Bin + A'B + BBin
![image](https://github.com/user-attachments/assets/a76a10d8-4a2a-481c-b9ee-b3685af24517)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




