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
**FULL ADDER:**


<img width="539" height="480" alt="398413823-c126f18a-c2d0-4395-8046-0c5982cf82f7" src="https://github.com/user-attachments/assets/3f7aebc6-b1dd-4413-b2aa-33cfebb120ca" />

**FULL SUBTRACTOR:**


<img width="558" height="495" alt="398413837-b5714c51-d131-4031-aa9f-e316bbc4deb8" src="https://github.com/user-attachments/assets/7183fece-ce6e-4f85-a238-149cca8e31d3" />

**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: SUDESAN T
RegisterNumber:25018208

     i)FULL ADDER
  
  module fa(a,b,cin,sum,carry);
  input a,b,cin;
  output sum,carry;
  assign sum=( (a ^ b)^cin);
  assign carry= ( (a & b)| ( cin &(a ^ b )));
  endmodule
  
  ii)FULL SUBTRACTOR
  
  module fs(a,b,bin,difference,borrow);
  input a,b,bin;
  output difference,borrow;
  assign difference= ( (a ^ b)^bin);
  assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
  endmodule
*/
```

**RTL Schematic**
<img width="1886" height="1026" alt="393964093-14c0b377-5b66-4f34-b7e2-21b3f7a5092e" src="https://github.com/user-attachments/assets/08c479bf-4d2b-4bd2-8c12-0013cae450d7" />
<img width="1866" height="948" alt="393964149-9bf1c529-04ab-4e86-a869-552fd2dd0a7b" src="https://github.com/user-attachments/assets/6b5ece29-4857-46d0-9fcc-f1837d590074" />


**Output Timing Waveform**
<img width="801" height="259" alt="398414023-651fa1e7-ad0f-49dc-8107-0ae5ce011ff5" src="https://github.com/user-attachments/assets/89082911-1197-4869-a270-1c9f395386ed" />
<img width="807" height="177" alt="398414033-e35e68b2-8946-4239-a10b-f8f430043794" src="https://github.com/user-attachments/assets/d78494d1-0f77-45bf-b606-7f2869ede76f" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



