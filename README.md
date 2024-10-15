# 4x4-Multiplier-Virtuoso

## Project Overview
This project implements a CMOS 4x4 Array Multiplier using fundamental logic components such as AND gates and 28-Transistor Mirror Full Adders. The focus of this design is to verify the correct functionality of the multiplier circuit without the inclusion of any low-power optimization techniques.

The project progressed in phases, starting from the basic building blocks of AND gates and Full Adders, culminating in the creation of a functional 4x4 multiplier. The design has been verified using Cadence Virtuoso, and the output waveforms have been analyzed to confirm accuracy.


Components Built:
AND Gate:

-Implemented basic CMOS AND gate using PMOS and NMOS transistors.
CMOS 28T Mirror Full Adder:

-Designed a Full Adder based on the 28-transistor mirror technique to achieve balanced performance for the carry and sum operations.
2x2 Multiplier:

-Built a basic 2x2 multiplier by combining the AND gates and Full Adders.
Verified the output waveform for various input combinations, confirming correct multiplication results.
4x4 Multiplier:

-Extended the 2x2 multiplier design to a 4x4 multiplier using an array multiplication approach.
The circuit was simulated, and output graphs were verified to be accurate.

![image](https://github.com/user-attachments/assets/eb96acd6-9e12-4f74-be27-d807999b0a88)

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

