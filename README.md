

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

**FULL AADER**

![WhatsApp Image 2024-12-21 at 9 58 41 AM](https://github.com/user-attachments/assets/7fe3c543-5930-4fa0-9caa-7e0829799c45)

**FULL SUBTRACTER**

![WhatsApp Image 2024-12-21 at 9 59 00 AM](https://github.com/user-attachments/assets/125395f4-ccfe-42aa-af2f-b325f70c91f9)

**PROCEDURE**

Write the detailed procedure here  
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:clarissa k RegisterNumber:24009830
*/

**FULL ADDER**
```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

```

**FULL SUBTRACTER**

```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule

```
**RTL Schematic**

**FULL ADDER**

![Screenshot 2024-11-05 083458](https://github.com/user-attachments/assets/08c54bde-fafe-4958-8f17-6cb9e54c7779)

**FULL SUBTRACTER**

![WhatsApp Image 2024-12-09 at 7 12 42 PM](https://github.com/user-attachments/assets/74ab2149-4503-4a30-b577-af05a3a1b61c)

**Output Timing Waveform**

**FULL ADDER**

![Screenshot 2024-11-05 083629](https://github.com/user-attachments/assets/33204b9b-5480-4375-9ae8-c7d74b6959f3)

**FULL SUBTRACTER**

![Screenshot 2024-11-05 085527](https://github.com/user-attachments/assets/a16c39ff-63de-4041-a0ba-d91c072d255f)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus II software.



