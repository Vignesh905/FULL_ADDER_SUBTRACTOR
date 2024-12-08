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
![Screenshot 2024-12-08 163726](https://github.com/user-attachments/assets/5225aa1e-e932-4bb4-80c1-35b6f8b9492a)
![Screenshot 2024-12-08 163745](https://github.com/user-attachments/assets/76de5dc8-9080-4f54-84cb-1ba1736f997c)

**Procedure**
1.  Type the program in the Quartus Software

2.  Compile and run the program

3.  Generate the RTL schematic and save the logic diagram

4.  Create nodes for inputs and outputs to generate the timing diagram

5.  For different input combinations generate this timing diagram

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by:PALLADI VENKATESH VIGNESH RegisterNumber: 24001645

      module exp4(sum, cout, a, b, cin);
      output sum;
      output cout;
      input a;
      input b;
      input cin;
      wire s1, c1, c2;
      xor(s1,a,b);
      and(c1,a,b);
      xor (sum, s1, cin);
      and (c2, s1, cin);
      or (cout, c2, c1);
      endmodule
      
      module exp4a (df, bo, a, b, bin);
      output df;
      output bo;
      input a;
      input b;
      input bin;
      wire w1,w2, w3;
      assign w1=a^b;
      assign w2=(~a&b);
      assign w3=(~w1&bin);
      assign df=w1^bin;
      assign bo=w2/w3;
      endmodule


**RTL Schematic**
![Screenshot 2024-12-08 163943](https://github.com/user-attachments/assets/b0f89aee-3dad-40a3-bf35-5183bd2311aa)

**Output Timing Waveform**
![Screenshot 2024-12-08 164022](https://github.com/user-attachments/assets/90b13df5-465e-4449-a0bc-53491f9faa29)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



