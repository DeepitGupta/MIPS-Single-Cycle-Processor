# 🧠 MIPS Single Cycle Processor (32-bit)

This project implements a **single-cycle 32-bit MIPS processor** in Verilog, developed as part of the **Hardware Lab coursework** at IIT Guwahati. It supports a minimal but functional set of MIPS instructions and simulates instruction execution at the gate-level.

## 🚀 Features

- ✅ **Arithmetic Operations**: `add`, `sub`, `and`, `or`, `slt`
- ✅ **Load/Store Instructions**: `lw`, `sw`
- ✅ **Branching and Control**: `beq`, `j`
- ✅ **Registers**: 32 general-purpose registers
- ✅ **Modular Design**: Clean separation of datapath and control logic
- ✅ **Gate-Level Simulation** using testbenches

## 📐 Architecture Overview

The processor is based on a **single-cycle datapath**, where each instruction completes in one clock cycle. The architecture includes:

- **ALU** – Performs arithmetic and logic operations
- **Register File** – 32 registers with read/write capabilities
- **Instruction Memory** – Stores input program in machine code
- **Data Memory** – For load/store operations
- **Control Unit** – Generates signals to coordinate datapath elements
- **Program Counter (PC)** – Tracks instruction execution

<p align="center">
  <img src="docs/mips-datapath.png" alt="MIPS Datapath" width="600"/>
</p>

> You can add your own datapath diagram under `/docs` and link it here.

## 🧪 Test Cases

Simulation was done using custom **testbenches** written in Verilog. Sample test programs cover:

- Arithmetic sequences
- Conditional branches
- Memory load/store operations

Example:
```assembly
add $t0, $t1, $t2     # t0 = t1 + t2
sw  $t0, 0($t3)       # store result in memory
beq $t0, $t1, LABEL   # branch if equal
