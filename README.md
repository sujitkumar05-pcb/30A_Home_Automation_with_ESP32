# 30A_Home_Automation_with_ESP32

## 1. Project Overview

30A Home Automation with ESP32 is a high-power IoT control system designed to safely switch electrical loads up to 30A. It uses the ESP32 for Wi-Fi–based remote control and automation. The complete schematic, PCB layout, and 3D design were developed in KiCad, with a strong focus on electrical isolation, proper track width, and safety for real-world applications.

-----

## 2. Key Learning Objectives

Understanding high-current (30A) PCB design and safety considerations

Practical experience with ESP32-based IoT hardware development

Schematic capture and multi-layer PCB layout using KiCad

Track width calculation, creepage & clearance implementation

Hardware testing, debugging, and design verification

Generating manufacturing (Gerber) and 3D output files

-----

## 3. Tools & Software Used
- **KiCad EDA**
  - Schematic Editor  
  - PCB Layout Editor  
  - 3D Viewer
 
 ---

## 4. Project Files
- Schematic design files (`.kicad_sch`)  
- PCB layout files (`.kicad_pcb`)  
- 3D render images  
- Manufacturing-ready Gerber files  

---

## 5. Block-Level Working Explanation

The system is powered by an AC mains supply, which is converted to a regulated DC voltage using a power supply module to safely operate the control circuitry. The ESP32 acts as the main controller, receiving user commands via Wi-Fi from a mobile or web application.

Based on these commands, the ESP32 drives an isolated switching stage (relay/contactor or solid-state device), ensuring safe separation between low-voltage control and high-current load circuits. The switching stage controls the connected 30A electrical load, turning it ON or OFF as required.

Protection components such as fuses, flyback diodes, and filtering circuits are included to enhance safety, reliability, and noise immunity. The system provides reliable remote control while maintaining electrical isolation and thermal safety.

## 6. Bill of Materials (BOM)
| Reference | Qty | Value / Part No.      | Footprint            | Datasheet / Notes |
| --------- | --- | --------------------- | -------------------- | ----------------- |
| C1        | 1   | 10 µF                 | C_0805_2012Metric    | –                 |
| C2        | 1   | 22 µF                 | C_0805_2012Metric    | –                 |
| D1, D4    | 2   | LED                   | LED_0805_2012Metric  | –                 |
| D2, D3    | 2   | 1N4148                | DO-35 (THT)          | Nexperia          |
| H1–H4     | 4   | Mounting Hole M2.5    | MountingHole_2.7 mm  | Excluded from BOM |
| J1        | 1   | 1×4 Pin Header        | PinHeader_2.54 mm    | –                 |
| J2        | 1   | 4-Pin Screw Terminal  | Phoenix MSTB 5.08 mm | –                 |
| J3        | 1   | 3-Pin Screw Terminal  | Phoenix MSTB 5.08 mm | –                 |
| K1        | 1   | RAYEX-L90AS Relay     | Relay_SPST_THT       | RAYEX             |
| K2        | 1   | PR13-5V-450-1C Relay  | Relay THT            | –                 |
| PS1       | 1   | HLK-PM01 AC–DC Module | Hi-Link_HLK-PMxx     | Hi-Link           |
| Q1, Q2    | 2   | S8050 Transistor      | TO-92                | –                 |
| R1–R6     | 6   | 1 kΩ                  | R_0805_2012Metric    | –                 |
| R7, R8    | 2   | 10 kΩ                 | R_0805_2012Metric    | –                 |
| SW1, SW2  | 2   | Push Button Switch    | 6 mm THT             | –                 |
| U1        | 1   | ESP32-WROOM-32        | RF_Module            | Espressif         |
| U2, U3    | 2   | PC817 Optocoupler     | DIP-4                | –                 |
| U4        | 1   | AMS1117-3.3           | TO-252-3             | –                 |


## 7. Images & Renders

- **Schematic**
<img width="1092" height="757" alt="image" src="https://github.com/user-attachments/assets/bb4d2298-0f27-4ea6-827a-09de2e3855cf" />

- **PCB Layout**
 <img width="415" height="438" alt="image" src="https://github.com/user-attachments/assets/c455ae4b-9067-498a-9a78-52477294b810" />
 <img width="417" height="437" alt="image" src="https://github.com/user-attachments/assets/2babe61f-75f1-46cf-b565-3895c2e836d2" />
 - **3D View**
<img width="895" height="853" alt="image" src="https://github.com/user-attachments/assets/91b236e9-19fb-48d6-a62c-44df982f3287" />

## 8. Disclaimer
This project is intended for educational and experimental purposes only. It involves high-voltage and high-current (up to 30A) circuits, which can be dangerous if handled improperly. The author is not responsible for any damage, injury, or loss resulting from the use, modification, or implementation of this design.

Users are advised to follow proper electrical safety standards, use appropriate protective components, and verify the design thoroughly before real-world deployment

---

## 9. Author
- **Name:** SUJIT KUMAR
- **Toolchain:** KiCad EDA  



