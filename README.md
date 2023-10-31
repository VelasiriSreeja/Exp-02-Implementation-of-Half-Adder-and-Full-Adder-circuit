# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: v.sreeja
RegisterNumber:  212222230169

For HALF ADDER:

module halfadder(a,b,s,c);
input a,b;
output s,c;
xor (s,a,b);
and (c,a,b);
endmodule

For FULL ADDER:

module fulladder(a,b,ci,s,co);
input a,b,ci;
output s,co;
wire d,e,f;
xor (d,a,b);
xor (s,d,ci);
and (e,ci,d);
and (f,a,b);
or (co,e,f);
endmodule
Logic symbol & Truthtable
RTL realization
/*

### Output:
1.Half Adder:

![Screenshot (360)](https://github.com/VelasiriSreeja/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118344328/5a55ae44-0e34-49a5-b166-648865fed89f)

2.Full Adder:

![Screenshot (361)](https://github.com/VelasiriSreeja/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118344328/1570f9fe-afbb-4f15-9046-01dd9efa13e1)


### TIMING DIAGRAM
1.Half Adder:

![Screenshot (362)](https://github.com/VelasiriSreeja/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118344328/a0c4d9c3-e064-4cd4-96e6-1281b623c438)

2.Full Adder:
 
![Screenshot (363)](https://github.com/VelasiriSreeja/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118344328/5b6224c0-17c1-4b18-a5ea-31ab4d1c26df)


### TRUTH TABLE 

1.Half Adder:

![Screenshot (376)](https://github.com/VelasiriSreeja/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118344328/f30e73b5-a304-4f42-ab89-84606caf647a)


2.Full Adder:

![Screenshot (377)](https://github.com/VelasiriSreeja/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118344328/e04aaade-14b2-4406-9c3b-d2616d1c5c4f)


### Result:
Thus half adder and full adder circuit is successfully designed and verified its truth table in
Quartus using Verilog programming.
