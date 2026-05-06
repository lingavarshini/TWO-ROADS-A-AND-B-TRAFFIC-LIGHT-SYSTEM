
# Two-Road Traffic Light Controller using FSM (Verilog)

## Overview
This project implements a two-road traffic light control system using a Finite State Machine (FSM) in Verilog. The controller manages traffic signals for Road A and Road B, ensuring safe and alternating traffic flow.

The design uses a counter-based delay mechanism to simulate realistic timing between light transitions.

---

## System Operation

The system cycles through the following sequence:

1. Road A → Green, Road B → Red  
2. Road A → Yellow, Road B → Red  
3. Road A → Red, Road B → Green  
4. Road A → Red, Road B → Yellow  

This sequence repeats continuously.

---

## Features
- Moore FSM-based design  
- Two-road traffic control system  
- Counter-based timing control  
- Clock-driven state transitions  
- Clean and modular Verilog implementation  
- Fully simulated using testbench  

---

## How It Works

### State Encoding
| State | Description |
|------|------------|
| 00 | Road A Green, Road B Red |
| 01 | Road A Yellow, Road B Red |
| 10 | Road A Red, Road B Green |
| 11 | Road A Red, Road B Yellow |

---

### Timing Logic
- A 26-bit counter generates delay  
- State transitions occur only when `count == 10` (simulation-friendly value)  
- This introduces controlled timing between traffic signals  

---

### Output Encoding
| Signal | Value | Meaning |
|--------|------|--------|
| 2'b10 | Green |
| 2'b01 | Yellow |
| 2'b00 | Red |

---

## Tools & Technologies
- Verilog HDL  
- Xilinx Vivado  
- Digital Design (FSM, Counters)  

---

## Project Structure
- `smart_traffic.v` → Main FSM design  
- `tb_smart_traffic.v` → Testbench for simulation  

---

## Simulation
1. Open project in Vivado  
2. Add design and testbench files  
3. Run behavioral simulation  
4. Observe waveform transitions for Road A and Road B  

---

## Key Concepts Demonstrated
- FSM design (Moore Machine)  
- State transition logic  
- Counter-based timing control  
- Multi-output digital system design  

---

## What I Learned
- Designing FSM for real-world applications  
- Synchronizing state transitions using counters  
- Managing multiple outputs in Verilog  
- Writing and verifying testbenches  

---

## Future Improvements
- Add pedestrian crossing signals  
- Implement adaptive traffic control using sensors  
- Deploy design on FPGA hardware  
- Replace fixed delay with configurable timing  

---

## Author
Linga
