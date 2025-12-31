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

Reference	Qty	Value		DNP	Exclude from BOM	Exclude from Board	Footprint	Datasheet
C1	1	10uF				Capacitor_SMD:C_0805_2012Metric	~	
C2	1	22uF				Capacitor_SMD:C_0805_2012Metric	~	
D1,D4	2	LED				LED_SMD:LED_0805_2012Metric	~	
D2,D3	2	1N4148				Diode_THT:D_DO-35_SOD27_P7.62mm_Horizontal	https://assets.nexperia.com/documents/data-sheet/1N4148_1N4448.pdf	
H1,H2,H3,H4	4	MountingHole_Pad		Excluded from BOM		MountingHole:MountingHole_2.7mm_M2.5_Pad_Via	~	
J1	1	Conn_01x04_Pin				Connector_PinHeader_2.54mm:PinHeader_1x04_P2.54mm_Vertical	~	
J2	1	Screw_Terminal_01x04				Connector_Phoenix_MSTB:PhoenixContact_MSTBVA_2,5_4-G-5,08_1x04_P5.08mm_Vertical	~	
J3	1	Screw_Terminal_01x03				Connector_Phoenix_MSTB:PhoenixContact_MSTBVA_2,5_3-G-5,08_1x03_P5.08mm_Vertical	~	
K1	1	RAYEX-L90AS				Relay_THT:Relay_SPST_RAYEX-L90AS	https://a3.sofastcdn.com/attachment/7jioKBjnRiiSrjrjknRiwS77gwbf3zmp/L90-SERIES.pdf	
K2	1	PR13-5V-450-1C				PR13-5V-450-1C:RELAY_PR13-5V-450-1C		
PS1	1	HLK-PM01				Converter_ACDC:Converter_ACDC_Hi-Link_HLK-PMxx	https://h.hlktech.com/download/ACDC%E7%94%B5%E6%BA%90%E6%A8%A1%E5%9D%973W%E7%B3%BB%E5%88%97/1/%E6%B5%B7%E5%87%8C%E7%A7%913W%E7%B3%BB%E5%88%97%E7%94%B5%E6%BA%90%E6%A8%A1%E5%9D%97%E8%A7%84%E6%A0%BC%E4%B9%A6V2.8.pdf	
Q1,Q2	2	S8050				Package_TO_SOT_THT:TO-92_Inline	http://www.unisonic.com.tw/datasheet/S8050.pdf	
R1,R2,R3,R4,R5,R6	6	1K				Resistor_SMD:R_0805_2012Metric	~	
R7,R8	2	10K				Resistor_SMD:R_0805_2012Metric	~	
SW1,SW2	2	SW_Push				Button_Switch_THT:SW_PUSH_6mm	~	
U1	1	ESP32-WROOM-32				RF_Module:ESP32-WROOM-32	https://www.espressif.com/sites/default/files/documentation/esp32-wroom-32_datasheet_en.pdf	
U2,U3	2	PC817				Package_DIP:DIP-4_W7.62mm	http://www.soselectronic.cz/a_info/resource/d/pc817.pdf	
U4	1	AMS1117CD-3.3				Package_TO_SOT_SMD:TO-252-3_TabPin2	http://www.advanced-monolithic.com/pdf/ds1117.pdf	

<img width="2177" height="501" alt="image" src="https://github.com/user-attachments/assets/8dab8155-4cdb-4027-9ede-9753c647b1ea" />


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



