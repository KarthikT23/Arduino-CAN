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

﻿MCP2515-----Arduino Uno	 
 
Vcc-----5V 	 

GND-----GND 	 

CS-----D10 	 

SO-----D12 	 

SI-----D11 	 

SCK-----D13 	 

INT(receiver)-----D2(receiver)	 

Also connect CAN_H and CAN_L of transmitter MCP2515 to CAN_H and CAN_L of receiver MCP2515

# Hardware Setup
![image](https://github.com/KarthikT23/Arduino-CAN/assets/119528503/cc5d69af-6591-4587-afb4-304008e8d246)



# Results
Messages on Serial monitor indicating that message has been successfully transmitted and Acknowledgement has been received
![image](https://github.com/KarthikT23/Arduino-CAN/assets/119528503/8ffb5cfa-e7e4-49e3-88aa-1a12e257944d)

Received messages on Serial Monitor
![image](https://github.com/KarthikT23/Arduino-CAN/assets/119528503/0c4df13b-b114-47ab-8217-9ca51dae3f65)

# References
[1] "Arduino CAN Bus Module Tutorial" by Julian Ilett: https://www.youtube.com/watch?v=e6f3T8WJzgI

[2] "Arduino CAN Bus Interface: What is it and How to Use it" by All About Circuits: https://www.allaboutcircuits.com/projects/arduino-can-bus-interface-what-is-it-and-how-to-use-it/

[3] "CAN-BUS Shield V2" Wiki page by Seeed Studio: https://wiki.seeedstudio.com/CAN-BUS_Shield_V2/

[4] "MCP2515 Datasheet" by Microchip Technology Inc.: https://ww1.microchip.com/downloads/en/DeviceDoc/20001801H.pdf

[5] "CAN Bus Protocol Tutorial" by Copperhill Technologies: https://copperhilltech.com/blog/can-bus-protocol-tutorial/

[6] https://www.tutorialspoint.com/can-bus-with-arduino

[7] "Design and Implementation of CAN Bus Communication System Based on Arduino", by Yunhao Li, published in the 2nd International Conference on Computer Science and Network Technology.

[8] "Implementation of a CAN Bus System Using Arduino", by James J. E. Hughes, published in the 2015 IEEE Global Humanitarian Technology Conference.


