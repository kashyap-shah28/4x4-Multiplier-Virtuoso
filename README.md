# 4x4-Multiplier-Virtuoso

## Project Overview
This project implements a standard array 4x4 multiplier using AND gates, and cmos28T mirror full adders. The design focuses on low-power optimization, leveraging GPDK180 technology with **multi-Vt** (multi-threshold) and **DVS** (Dynamic Voltage Scaling) techniques to be added further to achieve power efficiency. The multiplier will be verified through simulations for functionality, power, and timing analysis.

### Technology
- Process: GPDK180 (180 nm CMOS)
- Tools: Cadence Virtuoso (schematic entry, simulation, layout)
- Voltage: 1.8V (adjustable for DVS)

---

## Project Phases

### Phase 1: Circuit Design and Setup
1. **AND Gates and Full Adders**:
   - The basic building blocks (AND gates,  and full adders) are designed using minimum-sized transistors for low power.
   - Initial transistor parameters are selected based on typical GPDK180 values:
     - **Vt (Threshold Voltage)**: Standard, low, or high (to be tuned in later phases).
     - **Wp/Wn (Width of pMOS/nMOS transistors)**: Initial sizes set to **Wn = 180 nm**, **Wp = 360 nm**.

2. **Combining Partial Products**:
   - The 4x4 multiplier is built by combining partial products using AND gates.
   - The partial products are summed using half adders and full adders to produce the final result.

### Phase 2: Simulation and Power Analysis
1. **Schematic and Functional Verification**:
   - The full 4x4 multiplier circuit is assembled and simulated using **Cadence Virtuoso ADE**.
   - Functional tests are performed to verify that the circuit correctly multiplies two 4-bit numbers.

2. **Power and Timing Analysis**:
   - Static and dynamic power consumption is analyzed.
   - Timing analysis is performed to identify critical paths in the design.

---

## How to Run Simulations
1. **Environment Setup**:
   - Ensure that **GPDK180 technology** is properly installed in **Cadence Virtuoso**.
   - Set up the design environment by creating a new project and selecting GPDK180 as the process.

2. **Simulation Steps**:
   - Use **Virtuoso ADE** for simulation.
   - Run functional simulations using different sets of 4-bit inputs.
   - Perform power analysis using built-in ADE tools to check the total power consumption.

---

## Future Steps
- **Phase 3 (Upcoming)**: Apply **multi-Vt** optimization and **Dynamic Voltage Scaling (DVS)** to reduce power consumption, followed by final layout and parasitic extraction.

