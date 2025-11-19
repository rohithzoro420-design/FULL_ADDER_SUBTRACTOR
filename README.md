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

FULL ADDER:

<img width="358" height="234" alt="FULL ADEER" src="https://github.com/user-attachments/assets/4dd817f0-7fff-4837-8629-a67384a42bff" />

FULL SUBRACTOR:

<img width="455" height="475" alt="FULL" src="https://github.com/user-attachments/assets/35208c7b-bc94-4d62-8033-72049f455552" />

**Procedure**

.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**
Full ADDER :
~~~
module exp4 (a,b,d,s,c);
input a,b,d;
output s,c;
xor g1(s,a,b,d);
assign c=(a&b)|(b&d)|(d&a);
endmodule 
~~~
FULL SUBRACTOR :
~~~
module exp4 (a,b,c,d,b0);
input a,b,c;
output d,b0;
assign d=a^b^c;
assign b0=(a&b)|(c&(a^b));
endmodule 

~~~

**RTL Schematic**
FULL ADDER:

<img width="1660" height="1067" alt="Screenshot 2025-11-19 110526" src="https://github.com/user-attachments/assets/d978eca0-62e0-46a8-9ff9-aad1ab58726e" />

FULL SUBRACTOR:

<img width="1919" height="1079" alt="Screenshot 2025-11-19 112627" src="https://github.com/user-attachments/assets/25d69864-117f-4cc0-83b8-1097aa92c431" />


**Output Timing Waveform**
FULL ADDER:

<img width="1919" height="1079" alt="Screenshot 2025-11-19 110214" src="https://github.com/user-attachments/assets/3a6adceb-8233-44f1-8ac8-af89cfa614bc" />

FULL SUBRACTOR:

<img width="1918" height="1078" alt="Screenshot 2025-11-19 112603" src="https://github.com/user-attachments/assets/1272f5f3-ace8-4618-8315-72335fe60b92" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



