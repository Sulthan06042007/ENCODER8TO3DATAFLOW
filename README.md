### ENCODER 8TO3 DATAFLOW Modelling

**AIM:**

To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:** Quartus prime

**THEORY**

**Encoder 8 To 3**

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

**Truth Table**

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/35496b14-ae6e-4cd1-9abd-d6736b576575)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/95acaee6-c873-4c75-89eb-ef09fb158053)

Figure 02  Encoder 8 * 3

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
module exp5(a, b, c, y0, y1, y2, y3, y4, y5, y6, y7);
    input a, b, c;             // 3 input signals
    output y0, y1, y2, y3, y4, y5, y6, y7; // 8 output signals

    assign y0 = ~a & ~b & ~c;  // 000
    assign y1 = ~a & ~b &  c;  // 001
    assign y2 = ~a &  b & ~c;  // 010
    assign y3 = ~a &  b &  c;  // 011
    assign y4 =  a & ~b & ~c;  // 100
    assign y5 =  a & ~b &  c;  // 101
    assign y6 =  a &  b & ~c;  // 110
    assign y7 =  a &  b &  c;  // 111
endmodule
```
/* Program for Encoder 8 To 3 in Dataflow Modelling and verify its truth table in quartus using Verilog programming. 

Developed by: Ragul.K RegisterNumber:24006231
*/

**RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling**
![exp5](https://github.com/user-attachments/assets/ba40e9ad-461d-4621-b9d7-93f000785470)


**TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling**
![exp5-1](https://github.com/user-attachments/assets/06a8c39e-4304-42e0-bf47-00ffa100ef2b)

**RESULTS**
Thus Encoder 8 to 3 designed and truthtable is verified.



