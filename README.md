# LFSR-Based-Memory-System

##  Overview  
This project implements a **Linear Feedback Shift Register (LFSR) Based Memory System** using **SystemVerilog**. The system incorporates **memory management, LFSR for pseudo-random number generation, and top-level control logic**.

 **LFSR Implementation** – Generates pseudo-random sequences.  
 **Memory Storage and Access** – Data memory (`dat_mem.sv`) with controlled read/write.  
 **Testbench Validation** – Simulates system behavior and verifies correctness.  

---

##  Features  
- **Linear Feedback Shift Register (LFSR)** – Generates pseudo-random numbers for testing.  
- **Memory System** – Implements a **data memory module** for read/write operations.  
- **Top-Level Control** – Manages memory transactions and interactions.  
- **Testbench-Driven Verification** – Uses a **testbench (`Lab4_tb.sv`)** to validate functionality.  

---

##  File Structure  

| File | Description |  
|------|------------|  
| `dat_mem.sv` | Implements data memory storage and operations. |  
| `lfsr6.sv` | Implements a 6-bit LFSR for pseudo-random number generation. |  
| `top_level_starter.sv` | Manages system integration and top-level functionality. |  
| `Lab4_tb.sv` | Testbench for simulating and verifying system behavior. |  
| `Lab4Writeup.pdf` | Lab report detailing implementation, issues, and solutions. |  

---

##  Simulation & Testing  
### **Requirements**  
- **SystemVerilog Compiler** (e.g., ModelSim, QuestaSim, Quartus)  
- **Testbench Environment** for verifying behavior  

### **Running the Simulation**  
1️⃣ **Compile the SystemVerilog files**  
```sh
vlog dat_mem.sv lfsr6.sv top_level_starter.sv Lab4_tb.sv
```  
2️⃣ **Run the simulation**  
```sh
vsim -c -do "run -all" Lab4_tb
```  
3️⃣ **Check the waveform output** or **verify console logs**.  

---

##  Issues Encountered  
- **Clock Cycle Mismatch** – Original timing was off by 1-2 cycles, corrected through adjustments.  
- **Always Comb Block Gaps** – Some wires were missing assignments in certain cases, leading to Quartus issues.  
- **Complex Top-Level View** – The schematic turned out unexpectedly complex and needed debugging.  

---

##  Contributors  
- **Joachim Galil**  
- **Sean King** 
