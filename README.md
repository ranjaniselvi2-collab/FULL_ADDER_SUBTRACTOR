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

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
### Developed by: Ranjani.S

### RegisterNumber: 25017557

-------------------------------------
Full Adder
-------------------------------------
// Full Adder in Verilog
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule

------------------------------------
Full Sub
-------------------------------------
// Full Subtractor in Verilog
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule
**RTL Schematic**
<img width="1907" height="935" alt="Screenshot 2025-11-23 232939" src="https://github.com/user-attachments/assets/52bb2af8-b292-4a70-8551-67f2e424ce57" />
<img width="1907" height="970" alt="Screenshot 2025-11-23 234306" src="https://github.com/user-attachments/assets/68a09153-db16-422b-a5fa-aeb29e08377c" />

**Output Timing Waveform**
<img width="1907" height="1002" alt="Screenshot 2025-11-24 002517" src="https://github.com/user-attachments/assets/1361bc7b-f7d4-46e7-8f3c-0722a6421855" />
<img width="1822" height="946" alt="Screenshot 2025-11-24 001521" src="https://github.com/user-attachments/assets/1a06aed3-e522-487b-a1fb-ce5178f8b4b2" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



