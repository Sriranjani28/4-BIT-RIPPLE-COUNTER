# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

/* write all the steps invloved */
ALGORITHM: Step1: Define the specifications and initialize the design.
Step2: Declare the name of the entity and architecture by using VHDL
source code.
Step3: Write the source code in VERILOG.
Step4: Check the syntax and debug the errors if found, obtain the
synthesis report.
Step5: Verify the output by simulating the source code.
Step6: Write all possible combinations of input using the test bench.
Step7: Obtain the place and route report

**PROGRAM**

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.
module EX12( input wire clk, output reg [3:0] count );
always @(posedge clk) begin if (count == 4'b1111) count <= 4'b0000; else
count <= count + 1; end
endmodule
module RippleCounter_tb;
reg clk;
wire [3:0] count;
RippleCounter uut( .clk(clk), .count(count) ); initial begin clk = 0;
forever #5 clk = ~clk; end
initial begin #10;
$display("Time | Count"); $display("-----------------");
repeat (16) begin #5; $display("%4d | %b", $time, count); end
$finish; end
endmodule

 Developed by: Sriranjani.M
 
 RegisterNumber:24900016
*/

**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="480" alt="ex 12" src="https://github.com/user-attachments/assets/dfd10a0a-f970-47dc-88d1-c991a34fa8d6" />

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="463" alt="ex 12 timing diagram" src="https://github.com/user-attachments/assets/bf4d1648-8f6c-4f12-9394-057d4013f79d" />

**RESULTS**
Thus the OUTPUT’s of 4 Bit Ripple Counter are verified by synthesizing and simulating
the VERILOG code.
