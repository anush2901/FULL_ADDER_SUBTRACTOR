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
full adder

![image](https://github.com/user-attachments/assets/6308e1a5-3207-42b9-8ce2-3d183b23eb66)

full subtractor

![image](https://github.com/user-attachments/assets/962da18a-6843-4c1c-8362-07b60d225550)





**Procedure**

Full Adder: Open Quartus II and create a new project. Use schematic design entry to
draw the full adder circuit. The circuit consists of XOR, AND, and OR gates. Compile
the design, verify its functionality through simulation. Implement the design on the
target device and program it.
Full Subtractor: Follow the same steps as for the full adder. Draw the full subtractor
circuit using schematic design. The circuit includes XOR, AND, OR gates to perform
subtraction. Compile, simulate, implement, and program the design similarly to the
full adder


**Program:**

    //expt4a-full adder
    module ex4a(sum, cout, a, b, cin);
        output sum;
        output cout;
        input a;
        input b;
        input cin;
        
           wire w1,w2,w3;
           assign w1=a^b;
           assign w2=a&b;
           assign w3=w1&cin;
           assign sum=w1^cin;
           assign cout=w2|w3;
    endmodule
    
    //exp-4b-full subtractor
    module ex4b(df, bo, a, b, bin);
        output df;
        output bo;
        input a;
        input b;
        input bin;
        
           wire w1,w2,w3;
           assign w1=a^b;
           assign w2=(~a&b);
           assign w3=(~w1&bin);
           assign df=w1^bin;
           assign bo=w2|w3;
    endmodule

**RTL Schematic**
 full adder

 ![image](https://github.com/user-attachments/assets/ba68e390-5bc8-4fbb-859d-04c5fdb3ba2b)

full subtractor

![image](https://github.com/user-attachments/assets/ef1eae52-2605-48ab-80ca-dc1ca3eac546)


**Output Timing Waveform**
 full adder

![image](https://github.com/user-attachments/assets/951df368-b840-4731-86d3-7960dc04d5fe)

full subtractor

![image](https://github.com/user-attachments/assets/e2d299f9-6c56-4df1-8947-94bf7160f658)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



