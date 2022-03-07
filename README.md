Mixed Signal Circuit Design and Simulation Marathon

Design of Full Adder using Three Modelling Styles


ABSTRACT:
This paper describes the design and implementation of Full adder using VHDL results include
successful compilation of VHDL code in Quartus II ,waveforms shows verification of truth table , the result are
Also verified in analog domain using analog simulation it also show layout level implementation of full adder
using microwind tool, it also shows technological view of full adder along with chip floor plan. 


REFERENCE CIRCUIT DIAGRAM:
![Screenshot (81)](https://user-images.githubusercontent.com/101124509/157066189-4b5ac677-66d6-40fc-bf5e-f4db9934bdb3.png)



CIRCUIT DETAILS:
Full adder is a combinational circuit that has a ability to add two bits and a carry input and produces
sum bit and carry bit as output .full adder adds two bits A and B and carry from previous column called as carry
input.


TRUTH TABLE:

![Screenshot (84)](https://user-images.githubusercontent.com/101124509/157067622-055e2514-3036-48b5-9e3e-462f7a4900a0.png)


Software Used


eSim

It is an Open Source EDA developed by FOSSEE, IIT Bombay. It is used for electronic circuit simulation. It is made by the combination of two software namely NgSpice and KiCAD.
For more details refer:
https://esim.fossee.in/home


NgSpice

It is an Open Source Software for Spice Simulations. For more details refer:
http://ngspice.sourceforge.net/docs.html


Makerchip

It is an Online Web Browser IDE for Verilog/System-verilog/TL-Verilog Simulation. Refer
https://www.makerchip.com/


Verilator
It is a tool which converts Verilog code to C++ objects. Refer: https://www.veripool.org/verilator/


Circuit Diagram in eSim

The following is the schematic in eSim:

![Screenshot (85)](https://user-images.githubusercontent.com/101124509/157068882-d41b4d06-4ad4-4fd3-bd72-d76bcc8ffdc1.png)


Verilog Code:

architecture Structural of Full_Adder is
signal xor_1, and_1, and_2:STD_LOGIC;
 component XOR1 port(A, B : in STD_LOGIC;
 X: out STD_LOGIC);
 end component;
 component OR1 port(M, N : in STD_LOGIC; 
 Y: out STD_LOGIC);
 end component;
 component AND1 port(P, Q : in STD_LOGIC;
 Z: out STD_LOGIC);
 end component;
 begin
 X1:XOR1 port map(Input1, Input2, xor_1);
 X2:XOR1 port map(xor_1, Input3, Sum);
 A1:AND1 port map(Input1, Input2, and_1);
 A2:AND1 port map(xor_1, Input3, and_2);
 O1:OR1 port map(and_1, and_2, Carry);
end Structural;


VOLTAGE VS TIME RELATIONSHIP IN ANALOG DOMAIN:

![Screenshot (82)](https://user-images.githubusercontent.com/101124509/157070222-0a363968-1352-41d9-958c-8238b72aa0e7.png)



Acknowlegdements:
1.FOSSEE, IIT Bombay
2.Steve Hoover, Founder, Redwood EDA
3.Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalpghosh@gmail.com

References:
[1] Stephen Brown ,Fundamentals of digital logic with Verilog design(Tata McGRAW Hill)
[2] Jayaram Bhasker,A VHDL Primer (PTR Prentice Hall Englewood cliffs,New Jersey 07632)




