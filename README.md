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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber: S.SELVARANI : 212224040301
*/
## FULL ADDER
```
module fulladder(a, b, cin, sum, carry);
    input a;
    input b;
    input cin;
    output sum;
    output carry;
 assign sum=a^b^cin;
 assign carry=(a & b) | (b & cin) | (cin & a);
 endmodule

```

## FULL SUBTRACTOR
```
module fullsubtractor(a, b, cin, diff, borrow);
    input a;
    input b;
    input cin;
    output diff;
    output borrow;
	 wire abar;
	 assign abar= ~ a;
	 assign diff=a^b^cin;
	 assign borrow=(abar & b) | (b & cin) |(cin & abar);

endmodule
```


**RTL Schematic**\
## FULL ADDER
![Screenshot (201)](https://github.com/user-attachments/assets/6a32ee85-f024-4c88-b9c2-68ede3e563ef)
## FULL SUBTRACTOR
![Screenshot (203)](https://github.com/user-attachments/assets/7b16a2ae-4cf3-4e35-8ecd-0ba404e004e6)




**Output Timing Waveform**
## FULL ADDER 
![Screenshot (202)](https://github.com/user-attachments/assets/e8068e23-f3d5-485b-a706-0541b18073c4)

## FULL SUBTRACTOR
![Screenshot (204)](https://github.com/user-attachments/assets/7fb4dd4a-724f-4bc3-9737-b04d1f2cf68a)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



