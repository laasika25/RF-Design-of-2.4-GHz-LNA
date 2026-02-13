# 📡 RF Design of 2.4GHz Low Noise Amplifier (LNA)

[![Technology](https://img.shields.io/badge/Technology-45nm%20CMOS-blue)](https://en.wikipedia.org/wiki/CMOS)
[![Frequency](https://img.shields.io/badge/Frequency-2.4GHz-green)](https://en.wikipedia.org/wiki/2.4_GHz_radio_use)
[![Tool](https://img.shields.io/badge/Tool-Cadence%20Virtuoso-orange)](https://www.cadence.com/en_US/home/tools/custom-ic-analog-rf-design/circuit-design/virtuoso-analog-design-environment.html)

##  Project Overview

This project focuses on designing and optimizing a **Low Noise Amplifier (LNA)** operating at **2.4GHz** using **45nm CMOS technology** in Cadence Virtuoso. The LNA is designed to provide efficient reception of weak signals while maintaining optimal performance characteristics.

###  **What is an LNA?**
A Low Noise Amplifier is a critical component in RF systems that amplifies weak incoming signals while adding minimal noise. It's typically the first active component in a receiver chain, making its performance crucial for overall system sensitivity.

###  **Why 2.4GHz?**
The 2.4GHz ISM (Industrial, Scientific, and Medical) band is widely used for:
- 📶 **Wi-Fi** (802.11b/g/n)
- 🔵 **Bluetooth** communication
- 📡 **Zigbee** networks
- 🏠 **Smart home** devices
- 🎮 **Wireless gaming** controllers

This frequency band's popularity makes high-performance LNAs essential for modern wireless communication systems.

## Design Objectives

| Parameter | Target | Achieved |
|-----------|--------|----------|
| **Gain (S21)** | > 15 dB | 15-18 dB |
| **Noise Figure** | < 2 dB | Optimized |
| **Input Matching (S11)** | < -10 dB | Achieved |
| **Output Matching (S22)** | < -10 dB | Achieved |
| **Reverse Isolation (S12)** | < -30 dB | Excellent |
| **Power Dissipation** | < 50mW | 33mW |

## 🔬 Analysis Techniques

### 📊 S-Parameter Analysis
**Purpose**: Evaluate the amplifier's gain, input/output reflection, and reverse transmission characteristics.

**Configuration**:
- **Frequency Range**: 1 GHz to 5 GHz
- **Sweep Mode**: Automatic
- **Frequency Increment**: ~80 MHz
- **Analysis Type**: Small-signal AC analysis

**Key Parameters**:
- **S11 (Input Reflection)**: < -10 dB 
- **S21 (Forward Gain)**: 15-18 dB at 2.4 GHz 
- **S22 (Output Reflection)**: < -10 dB 
- **S12 (Reverse Isolation)**: < -30 dB 

### 🔊 Periodic Noise (Pnoise) Simulation
**Purpose**: Evaluate large-signal noise performance in periodic steady-state operation.

**Benefits**:
- Accounts for input noise, output noise, and noise transfer function
- Essential for time-varying RF circuits
- Provides accurate noise figure measurements
- Enables optimization of noise performance

## Power Analysis

### Power Dissipation Calculation
```
Supply Voltage (VDD) = 3.3V
Total Current = 10mA
Power Dissipation = VDD × I = 3.3V × 10mA = 33mW
```

**Result**: The LNA achieves excellent power efficiency with only **33mW** total power dissipation.

## 📈 Simulation Results

### 🔍 Noise Analysis Results
![Noise Analysis](https://github.com/user-attachments/assets/d774407a-184a-4904-95f3-b71af55e8d3d)
*Figure 1: Comparing output noise and input (Pnoise – periodic noise analysis)*

### 📡 S-Parameter Frequency Response
![S-Parameter Analysis](https://github.com/user-attachments/assets/e0b0e81b-bbb0-4572-a327-4d676c4c4e79)
*Figure 2: S-parameter analysis over 1-5 GHz frequency range with 80 MHz increments*

## 🛠️ Technology & Tools

###  Process Technology
- **Technology Node**: 45nm CMOS
- **Advantages**: 
  - Low power consumption
  - High integration density
  - Cost-effective manufacturing
  - Good RF performance

### Design Environment
- **Primary Tool**: Cadence Virtuoso
- **Simulation Types**: 
  - S-parameter analysis
  - Periodic noise simulation
  - AC analysis
  - DC analysis

## 📁 Project Structure

```
RF-Design-of-2.4GHz-LNA/
├── 📄 README.md                           # Project documentation
├── 📋 Cadence Virtuoso Step-By-Step Process.pdf  # Design methodology
├── 📊 VLSI DESIGN SKILLING PROJECT ABSTRACT -- LNA 2.4GHz.docx  # Project abstract
└── 📑 VLSI-Project Report 2.4GHz.docx    # Detailed project report
```

## 🎓 Learning Outcomes

This project demonstrates:
- **RF Circuit Design** principles
- **LNA Optimization** techniques
- **Noise Analysis** methodologies
- **S-Parameter** interpretation
- **Cadence Virtuoso** proficiency
- **CMOS Technology** understanding

## Future Enhancements

Potential improvements for future iterations:
- [ ] **Multi-stage LNA** design for higher gain
- [ ] **Wideband LNA** for broader frequency coverage
- [ ] **Power optimization** for battery-operated devices
- [ ] **Layout design** and parasitic extraction
- [ ] **Fabrication** and measurement validation

## References

- RF Microelectronics by Behzad Razavi
- CMOS Circuit Design, Layout, and Simulation by R. Jacob Baker
- Cadence Virtuoso Documentation
- IEEE RFIC Symposium Papers

---

**Made as part of Coursework in VLSI Design Project** - RF Design of 2.4GHz Low Noise Amplifier

---
