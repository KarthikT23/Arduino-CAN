# Arduino-CAN
CAN protocol communication between 2 Arduino Unos
# Hardware Components:
a) Two Arduino Uno boards

b) MCP2515 CAN controller module for each board

c) Jumper wires to connect the boards and the modules

# Software Components:
a) Arduino IDE

b) Libraries such as “mcp2515_can.h”, “SPI.h” etc.

# Arduino Uno
![image](https://github.com/KarthikT23/Arduino-CAN/assets/119528503/ef3d9bb5-bd32-4a27-86b8-323836e6039c)

# Arduino Uno Pinout
![image](https://github.com/KarthikT23/Arduino-CAN/assets/119528503/8ba0f202-c465-4ea3-ad23-e3a2ea296de2)

# Arduino IDE
![image](https://github.com/KarthikT23/Arduino-CAN/assets/119528503/b3bc1f1e-1d7d-4e65-bd0d-e14e26eab93e)

# MCP2515 Module
![image](https://github.com/KarthikT23/Arduino-CAN/assets/119528503/283a0a15-814e-4234-b091-ab0bd5ec3b85)

# Circuit Diagram
![image](https://github.com/KarthikT23/Arduino-CAN/assets/119528503/7f766bb3-3f94-4d5e-910e-75777da4d762)

﻿MCP2515 	      Arduino Uno	 
 
Vcc 	             5V 	 

GND 	             GND 	 

CS 	               D10 	 

SO 	               D12 	 

SI 	               D11 	 

SCK 	             D13 	 

INT (receiver) 	   D2 (receiver)	 

Also connect CAN_H and CAN_L of transmitter MCP2515 to CAN_H and CAN_L of receiver MCP2515

# Hardware Setup
![image](https://github.com/KarthikT23/Arduino-CAN/assets/119528503/b116b240-0ef2-4509-9d14-0625327ce066)

# RESULTS 
# # DSKOSA


