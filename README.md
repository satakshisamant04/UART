# UART Project – Verilog (Vivado)

This repository contains a UART (Universal Asynchronous Receiver/Transmitter) module implemented in Verilog using Xilinx Vivado. It enables serial communication by transmitting ASCII characters based on a configurable baud rate.

## 📁 Project Overview

- **Project File**: `UART.xpr`
- **Language**: Verilog HDL
- **Tool**: Xilinx Vivado
- **Core Modules**:
  - Baud rate generator
  - UART Transmitter (TX)
  - UART Receiver (RX)
  - Finite State Machines (FSMs)
  - Counters and multiplexers

## 🛠 Features

- Full UART transmission and reception for ASCII characters
- FSM-based design architecture for transmission control
- Baud rate generator for timing accuracy
- Designed for FPGA implementation
- Synchronous reset and positive-edge clocking

## 📂 File Structure

```
UART/
├── UART.xpr               # Vivado project file
├── src/                   # Verilog source files (FSM, UART TX/RX, etc.)
├── sim/                   # Testbench files
└── constraints/           # XDC constraints for FPGA board
```

## 🚀 How to Use

1. **Open Vivado**
2. Navigate to `File → Open Project` and select `UART.xpr`
3. Open the `src/` directory and review Verilog modules
4. Run synthesis, implementation, and simulation as needed
5. Use the testbench files in `sim/` to verify UART operation

## ✅ Requirements

- Xilinx Vivado (Version 2020.2 or later recommended)
- FPGA development board (for hardware testing)
- UART serial monitor (e.g., Tera Term, PuTTY)

## 🧪 Simulation

Simulation testbenches demonstrate:
- Correct transmission of ASCII data
- Timing accuracy at different baud rates
- Behavior under reset conditions

## ✍️ Authors

- Satakshi Dhal Samanta (NIT Rourkela)
