# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.
```
module EXP5_SISO(clk,clear,si,so);
input clk,si,clear;
output so;
reg so;
reg [3:0] tmp;
always @(posedge clk )
begin
if (clear)
tmp <= 4'b0000;
else
tmp <= tmp << 1;
tmp[0] <= si;
so = tmp[3];
end
endmodule
```
Developed by: RegisterNumber:sathiya priyan G 212225100048
<img width="1600" height="900" alt="WhatsApp Image 2026-09-13 at 23 51 15" src="https://github.com/user-attachments/assets/59d2e98d-b175-4417-b3fb-ce6bb26f3f02" />

*/

**RTL LOGIC FOR SISO Shift Register**
<img width="1600" height="900" alt="WhatsApp Image 2026-09-13 at 23 51 26" src="https://github.com/user-attachments/assets/4b7cfdf9-bd72-4438-89ec-70b66fcb6f62" />

**TIMING DIGRAMS FOR SISO Shift Register**
<img width="1600" height="900" alt="WhatsApp Image 2026-09-13 at 23 51 39" src="https://github.com/user-attachments/assets/53d3bebe-9b2d-40dd-8d5c-1de2029c77dd" />

**RESULTS**
The 4-bit SISO (Serial-In Serial-Out) shift register was successfully implemented using Verilog in Quartus Prime. The functionality was validated using the truth table. The shift register correctly shifted the input data one bit at a time through the flip-flops on each clock pulse. The outputs q0, q1, q2, and q3 were observed to propagate the input data as expected, confirming the correct operation of the shift register.****
