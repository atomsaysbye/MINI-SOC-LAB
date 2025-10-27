# 🧠 Simulated Mini SoC Lab

A **System-on-Chip (SoC)** design and verification environment created to simulate the key components of an embedded processor system.  
This project emulates the structure of a professional SoC lab — focusing on **CPU design, memory hierarchy, and peripheral interfacing** — without requiring virtual machines or proprietary EDA tools.

---

## 🚀 Overview

This lab models the core principles of SoC development using HDL-based design flows.  
It includes modular Verilog source files, testbenches, and example scripts that illustrate the design process of a **minimal RISC-style processor** integrated with basic peripherals and memory subsystems.

> ⚙️ While this repository does not run on actual EDA tools, it represents a *realistic structure and documentation* of a hardware design workflow suitable for educational and portfolio purposes.

---

## 🧩 System Architecture

The Mini SoC comprises:
- **CPU Core** — 16-bit RISC architecture with ALU, control unit, and register file  
- **Memory System** — Separate instruction and data memory with a memory controller  
- **Peripherals** — UART, GPIO, and Timer modules  
- **Bus Interface** — Simplified bus for internal communication  

<p align="center">
  <img src="docs/architecture_diagram.png" alt="Architecture Diagram" width="600">
</p>

---

## 📂 Directory Structure

| Directory | Description |
|------------|-------------|
| `src/` | HDL source files for CPU, memory, and peripherals |
| `tb/` | Testbenches for each subsystem and full SoC verification |
| `scripts/` | Example shell scripts to simulate compile/run workflow |
| `docs/` | Architecture diagrams, design notes, and results summary |
| `reports/` | Placeholder synthesis and timing reports |

---

## 🧠 Design Highlights

- **ALU** supports 8 arithmetic and logic operations  
- **Control Unit** implements a single-cycle instruction decode mechanism  
- **Register File** with two read ports and one write port  
- **Memory Controller** manages synchronous read/write access  
- **UART Peripheral** demonstrates serial communication interface  

---

## 🧪 Simulation (Conceptual)

Simulation scripts are provided for educational demonstration.  
Example workflow (non-executable but realistic):

```bash
# Compile design files
./scripts/compile.sh

# Run top-level SoC testbench
./scripts/run_tests.sh

# View waveform (if using ModelSim or GTKWave)
vsim -do scripts/wave_viewer.do
