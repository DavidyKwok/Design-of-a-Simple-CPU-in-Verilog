# Design-of-a-Simple-CPU-in-Verilog
A Simple CPU that contains Latches, ALU, FSM, and decoder in Verilog, simulated using Vivado to perform various arithmetic and logical operations displaying results on 7-segment displays.

## Features
- **Mealy State Machine**: Handles control logic for the CPU's operation.
- **ALU**: Performs arithmetic and logical operations.
- **Decoder**: Decodes FSM outputs into control signals.
- **Seven-Segment Display**: Displays results of operations and error states.
- Modular design with separate files for each major component.

### Design Details
__________________
#### FSM (Finite State Machine)
- Implements a Mealy state machine to control CPU operations based on the input signal and clock cycles.

#### ALU (Arithmetic Logic Unit)
- Performs basic arithmetic (addition, subtraction) and logical operations (NAND, NOR, XOR, etc.).

#### Decoder
- Translates the FSM state into control signals for the ALU.

#### Seven-Segment Display (SSEG)
- Converts binary outputs from the ALU into human-readable digits displayed on a seven-segment display.

## Block Diagram ##
![Screenshot 2025-01-04 153939](https://github.com/user-attachments/assets/3e093fb4-e86e-40ca-8dec-ac4f7bc88fec)

## Simulation Results

### CPU Testbench ###
_____________________
![image](https://github.com/user-attachments/assets/f610f1e9-f08e-4b80-96b7-f8f26a6ebdaa)
### Predicted Results ###
_________________________
a = 2, b = 1
- State 0 | Operation: Addition | Result: out1 = 01 (0), out2 = 06 (3) |
- State 1 | Operation: Subtraction | Result: out1 = 01 (0), out2 = 4f (1) |
- State 2 | Operation: Not a | Result: out1 = 4f (1), out2 = 06 (3) |
- State 3 | Operation: NAND | Result: out1 = 4f (1), out2 = 24 (5) |
- State 4 | Operation: NOR | Result: out1 = 4f (1), out2 = 12 (2) |
- State 5 | Operation: AND | Result: out1 = 01 (0), out2 = 01 (0) |
- State 6 | Operation: XOR | Result: out1 = 01 (0), out2 = 06 (3) |
- State 7 | Operation: XNOR | Result: out1 = 4f (1), out2 = 12 (2) |
  
![image](https://github.com/user-attachments/assets/2200b3b1-ec0c-44e0-ab00-9f15b2f4a598)

