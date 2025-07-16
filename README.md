# UART Transmitter with Debouncing – Verilog (Basys 3, Vivado)

This project implements a UART (Universal Asynchronous Receiver/Transmitter) transmitter in Verilog, with a debouncing circuit to enable clean button-triggered data transmission from an FPGA board.

## 📌 Overview

- **Language**: Verilog HDL  
- **Platform**: Basys 3 FPGA Board  
- **Tool**: Xilinx Vivado  
- **Features**:
  - UART transmission using 8N1 format (8 data bits, no parity, 1 stop bit)
  - Button debouncing to eliminate mechanical glitches
  - Transmission of a fixed ASCII character ('S') upon each button press

## 📁 Project Structure

├── transmitter.v # UART transmission logic
├── transmit_debouncing.v # Button debounce module
├── top.v # Top-level integration of TX and debounce
├── Basys3_Master.xdc # Constraint file for pin mapping
├── UART.xpr # Vivado project file


## 🛠 Key Modules

- **transmitter.v**: Handles UART byte serialization using a state machine and controlled timing (via ticks).
- **transmit_debouncing.v**: Eliminates button bounce by sampling input over time and issuing a single clean pulse.
- **top.v**: Connects the modules and maps I/O for the Basys 3 board (button input and UART TX output).

## ▶️ How to Run

1. Open the project in **Vivado** using `UART.xpr`.
2. Synthesize and implement the design.
3. Generate bitstream and program the Basys 3 board.
4. Press the assigned button to transmit `'S'` over the UART TX line.

## 🧰 Tools Required

- Xilinx Vivado (2020.2 or later)
- Basys 3 FPGA Board
- UART serial monitor (e.g., Tera Term, PuTTY)

## 📬 Output

- Every button press sends the ASCII character `'S'` (0x53) over the UART line.
- The transmission follows standard UART protocol: 1 start bit, 8 data bits, 1 stop bit.

## ✍️ Author- Satakshi Dhal Samanta (NIT Rourkela)
