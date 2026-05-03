# IoT-Predictive-Maintenance-Unit
An ESP32-based IoT system for motor fault detection using acoustic analysis, FFT, and real-time monitoring via Telegram and OLED display
# IoT-Predictive-Maintenance-Unit 🛠️🔊

An advanced ESP32-based IoT system designed for **Predictive Maintenance** of industrial motors. This unit utilizes acoustic signal analysis and Fast Fourier Transform (FFT) to detect mechanical anomalies before they lead to system failure.

---

## 🚀 Overview
Predictive maintenance is the future of industrial efficiency. This project integrates hardware and software to monitor motor health in real-time. By analyzing frequency spectrums, the system identifies specific fault patterns such as bearing wear, misalignment, or imbalance.

### Key Features
*   **Acoustic Fingerprinting:** Captures motor sound using a high-sensitivity analog microphone.
*   **On-Device DSP:** Performs Real-time Fast Fourier Transform (FFT) to analyze frequency components.
*   **Dual-Layer Monitoring:** 
    *   **Local:** 0.96" I2C OLED display for immediate status updates.
    *   **Remote:** Telegram Bot integration for instant alerts and remote telemetry.
*   **Industrial Grade Power:** Dedicated PCB with dual Mini360 buck converters for high-efficiency voltage regulation (5V and 3.3V rails).
*   **Environmental Awareness:** Integrated LDR for ambient light sensing and system status indicators.

---

## 🛠️ Hardware Architecture
The hardware is designed for reliability and signal integrity.

### PCB Design Specifications
*   **Processor:** ESP32-WROOM-32 (Dual-core for simultaneous DSP and WiFi tasks).
*   **Power Management:** Dual Mini360 Buck Converters for stable power delivery.
*   **Protection:** Decoupling capacitors (100uF) on power rails to filter motor-induced noise.
*   **User Interface:** Tactile buttons for manual resets/mode switching and a 10K potentiometer for sensitivity calibration.

> [!TIP]
> All engineering files including **Schematics (PDF)**, **BOM (CSV)**, and **Gerber Files** for production are located in the `/PCB_Design` folder[cite: 1].

---

## 📂 Repository Structure
```text
├── Firmware/             # C++/Arduino source code (FFT & IoT Logic)
├── PCB_Design/           
│   ├── Predictive_Maintenance_System_PCB.pdf   # Technical Schematics[cite: 1]
│   ├── BOM_Predictive_Maintenance_V1.csv       # Bill of Materials
│   ├── Gerber_PCB1_2026-05-03.zip             # Manufacturing Files
│   └── Images/                                 # 3D Renders & PCB Photos[cite: 1]
└── README.md
