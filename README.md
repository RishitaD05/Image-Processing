# Image Blurring on PYNQ-Z2 using FPGA Hardware Acceleration and Linux-Python Processing

## Project Overview
This project implements a grayscale image blurring pipeline on the **PYNQ-Z2 (Zynq-7000 SoC)** using two approaches:

- **FPGA Hardware Acceleration (PL)** using Verilog HDL in Xilinx Vivado  
- **Software-Based Processing (PS)** using Python on ARM-Linux via the PYNQ framework  

The project aims to study the performance benefits of FPGA acceleration compared to software execution on the ARM processor.

---

## Tools & Technologies
- Xilinx Vivado
- Verilog HDL
- Python
- Jupyter Notebook
- PYNQ Framework
- Zynq-7000 SoC (ARM + FPGA)

---

## Hardware Platform
- **Board:** PYNQ-Z2  
- **SoC:** Xilinx Zynq-7000 (ARM Cortex-A9 + FPGA Fabric)  
- **Execution Environment:** PYNQ Linux + Jupyter Notebook  

---

## Project Objectives
- Implement grayscale image blurring using both FPGA hardware and ARM software approaches
- Design a convolution-based blur accelerator in FPGA fabric
- Develop a Python-based blur algorithm on ARM Linux
- Compare hardware vs software implementation in terms of latency and throughput

---

## Implementation Details

### FPGA Hardware Accelerator (PL)
- Designed and implemented a **3×3 convolution-based blur accelerator** in Verilog HDL
- Targeted **512×512 grayscale images**
- Implemented in Vivado and deployed on the FPGA fabric
- Supports streaming-style processing for faster throughput

### Linux-Python Software Implementation (PS)
- Implemented blur filtering using Python on ARM Cortex-A9 running Linux
- Used a **5×5 convolution kernel**
- Executed via Jupyter Notebook using the PYNQ framework
- Provides a software reference model for performance comparison

---


---

## FPGA Hardware Flow (Vivado + PYNQ)
1. Design the 3×3 blur convolution accelerator in Verilog HDL  
2. Integrate the accelerator into a Vivado block design  
3. Generate the `.bit` and `.hwh` files  
4. Load the hardware overlay in PYNQ using Python  
5. Execute the blur accelerator in programmable logic (PL)

---

## Software Flow (Python on ARM-Linux)
1. Load grayscale image in Python  
2. Apply a 5×5 blur convolution filter  
3. Generate and store blurred output image  
4. Use output as baseline reference for FPGA comparison  

---

## Key Features
- Dual implementation: FPGA hardware + ARM software
- Hardware accelerator uses 3×3 convolution kernel
- Software implementation uses 5×5 convolution kernel
- Target image size: 512×512 grayscale
- Designed and executed on real Zynq SoC hardware using PYNQ

---

## Future Work
- Perform performance comparison of hardware vs software execution
- Analyze:
  - Latency
  - Throughput
  - FPGA acceleration benefits
- Optimize hardware design using pipelining and improved memory interfacing
- Study FPGA resource utilization and timing results

---

## Learning Outcomes
- Gained experience in FPGA-based image processing design flow
- Understood PS-PL integration on Zynq SoC using PYNQ framework
- Designed convolution accelerator in Verilog HDL
- Implemented software reference model in Python
- Learned performance evaluation methodology for hardware acceleration

---



