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

<img width="894" height="740" alt="image" src="https://github.com/user-attachments/assets/40862e4f-1e9e-4dc9-88b3-aa9fb509dd3b" />


## 7. Images & Renders

- **Schematic**
 <img width="1156" height="802" alt="image" src="https://github.com/user-attachments/assets/58c0e51d-bcfa-410f-92cf-de941da9adf7" />


- **PCB Layout**

 <img width="435" height="464" alt="image" src="https://github.com/user-attachments/assets/5e5f7598-d853-430d-8f61-1186618ec744" />
<img width="437" height="465" alt="image" src="https://github.com/user-attachments/assets/523bfe6b-55ca-461c-9c3a-f0bd94e4d66e" />

- **3D View**
  
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e6aea03b-88b7-43d5-882f-bd5dd21f23fd" />
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/99e1a283-d1b9-42d0-bef6-dfff281cc5e9" />

---

## 8. Disclaimer
This project is intended for educational and experimental purposes only. It involves high-voltage and high-current (up to 30A) circuits, which can be dangerous if handled improperly. The author is not responsible for any damage, injury, or loss resulting from the use, modification, or implementation of this design.

Users are advised to follow proper electrical safety standards, use appropriate protective components, and verify the design thoroughly before real-world deployment

---

## 9. Author
- **Name:** SUJIT KUMAR
- **Toolchain:** KiCad EDA  



