# Single-Cycle RISC Processor

## Overview

This repository contains a complete implementation of a single-cycle RISC (Reduced Instruction Set Computer) processor designed using VHDL. The processor executes one instruction per clock cycle, making it a fundamental educational implementation for understanding computer architecture principles.

## Architecture

The processor is composed of several interconnected modules that work together to fetch, decode, and execute instructions. Each component is designed to handle specific aspects of instruction processing.

## Components

### Core Processing Units

- **ALU (Arithmetic Logic Unit)**: Performs arithmetic and logical operations on operands
- **ALU Control Unit**: Generates control signals for the ALU based on instruction opcodes and function codes
- **Control Logic Unit**: Main control unit that generates control signals for the entire processor datapath

### Memory Components

- **Instruction Memory (instrmem)**: Stores program instructions to be executed
- **Data Memory (datamem)**: Stores data values that can be read from or written to during program execution

### Data Path Components

- **Register File**: Contains general-purpose registers for storing operands and results
- **Eight-Bit Register**: Single register component for temporary storage
- **ENARDFF_2**: Enabled register with D flip-flop implementation

### Arithmetic and Logic Units

- **Eight-Bit Adder**: Performs addition operations on 8-bit operands
- **Eight-Bit Add/Subtract**: Combined unit capable of both addition and subtraction
- **Eight-Bit Comparator**: Compares two 8-bit values and generates comparison results
- **Thirty-Two-Bit Adder**: Extended precision adder for address calculations

### Multiplexers

- **One-Bit Multiplexers**: 2-to-1, 5-to-1, and 6-to-1 multiplexers for single-bit signal routing
- **Eight-Bit Multiplexers**: 2-to-1, 5-to-1, 6-to-1, and 8-to-1 multiplexers for 8-bit data path routing
- **Three-Bit 2-to-1 Multiplexer**: Used for register selection

### Supporting Components

- **Shift Left 2 Units**: Performs left shift by 2 positions for address calculation
- **Three-to-Eight Decoder**: Decodes 3-bit inputs to 8 output lines

### Testbenches

The repository includes comprehensive testbenches for verification:
- Testbench for ALU
- Testbench for ALU Control Unit
- Testbench for Control Logic Unit
- Testbench for Eight-Bit Add/Subtract
- Testbench for Single-Cycle Processor

## Design Files

Each component directory contains:
- RTL (Register Transfer Level) design files
- Structural design files where applicable
- Synthesis files for implementation
- Primary database files for project management

## Usage

This project was developed using ModelSim/Quartus II for simulation and synthesis. The design files are in VHDL format and can be compiled and simulated using standard VHDL simulation tools.

## Project Structure

The project is organized into directories corresponding to each major component, with each directory containing the necessary design files, synthesis outputs, and project metadata.

## Educational Context

This implementation serves as an educational resource for understanding:
- Single-cycle processor architecture
- Instruction fetch, decode, and execute cycles
- Datapath and control unit design
- VHDL hardware description language
- Digital system design principles

## License

This project is provided for educational purposes.
