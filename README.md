# A Minimum Phase Single-Input Dual-Output Buck and Buck–Boost DC-DC Converter for DC Microgrid application

This repository contains MATLAB/Simulink modeling, simulation, and controller design for a **minimum-phase dual-output DC–DC converter** based on the IEEE paper:

**“Dual-Output Classic Buck and Buck–Boost Converter with Fast Dynamic Response”**

The converter produces:
- **Positive Buck Output**
- **Negative Buck–Boost Output**

from a **single DC input**, using two duty cycles *(D and d₁)*.

This work is part of my **B.Tech Project (BTP)** at **IIT Patna**, under the supervision of **Dr. Bussa Vinod Kumar**.
## 🚀 Project Overview

The objective of this project is to:

- Understand the converter operation and switching modes  
- Derive plant transfer functions via small-signal state-space modeling  
- Reproduce the converter's behavior through open-loop simulations  
- Implement **PI–Lead compensators** for closed-loop control  
- Validate performance under input, load, and reference variations  

The converter eliminates the **Right-Half-Plane Zero (RHPZ)** in the buck–boost output, achieving **minimum-phase behavior** and improved transient performance.

## ⚡ Features Implemented
### ✔ 1. Open-Loop Converter Simulation
- Full switching-cycle analysis (three modes)
- Inductor, diode, and switch current waveforms
- Validation of theoretical voltage gains:
  - Buck Output: **Mo₁ = D**
  - Buck–Boost Output: **Mo₂ = D / (1 − D − d₁)**

---
   

### ✔ 2. Small-Signal Modeling & Transfer Functions
Derived transfer functions:
- **G_vov** — input-to-output
- **G_vod** — duty-to-output

Confirmed:
- Buck output is minimum-phase  
- Buck–Boost output has **no RHP zero**

---

### ✔ 3. Closed-Loop Control Using PI–Lead Compensators
Separate PI–Lead controllers were designed for:

#### ➤ Buck Output
- Crossover frequency ≈ **1.7 kHz**  
- Phase margin ≈ **30°**

#### ➤ Buck–Boost Output
- Crossover frequency ≈ **500 Hz**  
- Phase margin ≈ **30°**

Benefits:
- Faster transient response  
- Improved phase margin  
- Zero steady-state error  

---

### ✔ 4. Closed-Loop Validation
Tested under:

- **Input voltage variation**  
- **Reference voltage steps**  
- **Load disturbances**  

System maintained stable and accurate voltage regulation.


## 🔧 Software Requirements

- MATLAB R2021b or later  
- Simulink  
- Control System Toolbox  


## 🧠 Learning Outcomes

- State-space modeling of power electronic converters  
- Deriving transfer functions from averaged models  
- Stability analysis using Bode plots  
- Designing PI–Lead compensators  
- Implementing dual-output control loops  
- Understanding RHPZ elimination techniques  
- Building full MATLAB/Simulink workflows


## 📘 Reference Paper

Hasanpour, S., Mostaan, A., & Haghighi, S. K. S. (2024).  
**Dual-Output Classic Buck and Buck–Boost Converter with Fast Dynamic Response**.  
IEEE Journal of Emerging and Selected Topics in Industrial Electronics.


## 🛠️ Future Work

- Hardware prototype development  
- Component selection (MOSFETs, inductors, capacitors)  
- Controller implementation on STM32 / DSP / Arduino  
- Real-time testing and efficiency measurement  
- Comparison with simulation results  


## 📄 License

This project is released under the **MIT License**.  
You are free to use, modify, and distribute the code.

## ⭐ Author

**Y. Tharun Teja**  
B.Tech Electrical Engineering  
Indian Institute of Technology Patna  


