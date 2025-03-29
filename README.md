# Bottle Return Center Simulation – AnyLogic Model

## Overview
This repository contains a complete **Discrete Event Simulation (DES)** developed in **AnyLogic** to model a **Bottle Return and Recycling Center**, as part of the final assessment for **MATH5007 – Simulation & Optimization** at Curtin University. The simulation focuses on modeling real-world customer flow, resource management, and queue optimization in a high-demand recycling environment.

---

## 🎯 Objective
- Simulate customer arrival, bottle returns, and payment processes
- Track system performance: customer wait times, machine/worker utilization, queue lengths
- Evaluate bottlenecks and suggest optimal resource configurations
- Propose improvements based on measurable KPIs (lost customers, service time, efficiency)

---

## 🧩 Simulation Design
- **Resources Modeled**:
  - `MachinePool`: Bottle return machines
  - `WorkerPool`: Staff assisting customers and managing payments
- **Customer Flow**:
  - Customers enter → choose service → return bottles → receive payment → exit
- **Queuing System**:
  - Wait lines at machine return, direct service, and payment counters
  - Exit tracking for customers who leave due to delay or unavailability
- **Time Tracking**:
  - Implemented `TimeMeasureStart` and `TimeMeasureEnd` across phases
  - Calculated total system time and bottleneck-specific intervals

---

## 📈 Experimental Results
### 🔹 Default Configuration:
- MachinePool = 1 | WorkerPool = 1
- Machine Utilization: **99%**
- Worker Utilization: **53%**
- Lost customers due to queue: **287**
- Bottles returned (packed batches): **15**

### 🔹 Optimized Scenario:
- MachinePool = 3 | WorkerPool = 2
- Machine Utilization: **95%**
- Worker Utilization: **79%**
- Lost customers due to queue: **26**
- Total paid customers: **428**

### 🔹 Final Enhancement:
- MachinePool = 3 | WorkerPool = 3
- Payment queue cleared; customer wait times minimized
- Still cost-efficient without excessive idle resource time

---

## 🔍 Proposed Model Improvements
1. **Stage-wise Time Breakdown**: Time measurements at each stage for granular performance tracking
2. **Dynamic Routing**: Redirect overflow customers from machines to direct service
3. **Dual Payment Counter**: Add automated machine-based payout option (ATM-style resource)

---

## 📁 Repository Contents
| File | Description |
|------|-------------|
| `20972008_Zaidi_WordAnswers.docx` | Full project report and simulation explanation |
| `*.alp` (Not included) | AnyLogic simulation file (not uploaded here) |
| `Screenshots/` | Optional visualization charts (if added) |

---

## 🛠 Tools Used
- **Software**: AnyLogic (DES & simulation modeling)
- **Model Elements**: Source, Queue, Delay, SelectOutput, TimeMeasure, ResourcePool
- **Visuals**: Histograms, Pie Charts, Utilization plots, Time plots

---

## 👤 Author
**Syed Muhammad Ahmed Zaidi**  
Curtin University – MATH5007 (Simulation & Optimization)  
Student ID: 20972008

---

## License
For educational use only. Commercial replication or use requires permission.

---

## Status
✅ Completed | 🧪 Optimized & Tested | 📊 Ready for further implementation or research use
