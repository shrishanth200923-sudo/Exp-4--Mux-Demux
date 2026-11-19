# Exp-4-Mux-Demux
# Design and Verification of 2:1 Multiplexer and 1:2 Demultiplexer
## Aim
To design and verify a 2:1 Multiplexer and a 1:2 Demultiplexer using Verilog HDL.
## Theory / Synopsis
A 2:1 Multiplexer (MUX) selects one of two data inputs, A or B, and routes it to a single output Y based on the value of the select line S. A 1:2 Demultiplexer (DEMUX) performs the reverse operation: it routes a single data input D to one of two outputs, Y0 or Y1, based on the select line S.
Boolean Functions
### 2:1 Multiplexer:
•	Y = S'.A + S.B
### 1:2 Demultiplexer:
•	Y0 = S'.D
•	Y1 = S.D
## Files to be Created

<img width="575" height="65" alt="image" src="https://github.com/user-attachments/assets/04c2d90c-0b6b-4b35-b603-d0e10e1e4f00" />

## Design / RTL Program

```
## **Testbench Program



## Truth Table

### 2:1 Multiplexer

<img width="573" height="154" alt="image" src="https://github.com/user-attachments/assets/96dd3fa2-7747-402d-b88f-17c11e28fcbb" />

### 1:2 Demultiplexer

<img width="583" height="90" alt="image" src="https://github.com/user-attachments/assets/4bc21b52-1db5-4302-afab-ebb0b9d5a74b" />

## Simulation Procedure

STEP 1 – Open Terminal
Open a terminal in the experiment folder.

STEP 2 – Load Synopsys Environment
source /synopsys/start.sh

STEP 3 – Compile Using VCS
vcs mux_demux.v mux_demux_tb.v -full64
If compilation is successful, VCS generates the simulation executable:
simv

STEP 4 – Run Simulation
./simv
The terminal displays the input combinations and corresponding outputs Y, Y0, and Y1.
A VCD waveform file is also generated:
mux_demux.vcd

STEP 5 – Open DVE

dve -full64
Other option
dve -full64 &
A DVE environment will open.
DVE Waveform Verification
In DVE:
•	Open the testbench hierarchy.
•	Locate the signals:
o	A
o	B
o	S
o	Y
o	D
o	Y0
o	Y1
•	Add the signals to the waveform window.
•	Run/inspect the waveform.
•	Verify that Y = A whenever S = 0, and Y = B whenever S = 1.
•	Verify that Y0 = D and Y1 = 0 whenever S = 0, and Y1 = D and Y0 = 0 whenever S = 1.
•	Confirm that Y0 and Y1 are never both high at the same time, since only one output is active per select value.
The waveform should agree with the truth table.

## Expected Result

The 2:1 Multiplexer and 1:2 Demultiplexer were realized using Verilog HDL:

•	Y = S'.A + S.B
•	Y0 = S'.D, Y1 = S.D

The design was compiled and simulated using Synopsys VCS, and the functionality was verified using DVE waveform analysis, matching the expected truth table.

## Output


<img width="1853" height="896" alt="Screenshot 2026-11-19 152850" src="https://github.com/user-attachments/assets/5ed1eb73-d36b-4b5d-8f5c-f72a329b8d4b" />


Thus, the 2:1 Multiplexer and 1:2 Demultiplexer were designed, implemented using Verilog HDL, successfully simulated using Synopsys VCS, and verified using Synopsys DVE.



