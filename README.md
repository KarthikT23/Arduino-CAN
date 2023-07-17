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

# Transmitter Code Explanation:
1) The code is for implementing CAN bus communication between two Arduino Uno boards using the MCP2515 module. The MCP2515 module is connected to the Arduino Uno through SPI communication using the mcp2515_can library.

2) In the setup() function, the serial communication is initiated and the MCP2515 module is initialized with a baud rate of 500Kbps. A loop is added to keep retrying the initialization process until it is successful.

3) In the loop() function, a message is sent using the CAN.sendMsgBuf() function with an ID of 0x00, a standard frame, a data length of 3, and a data buffer stmp. The stmp buffer is incremented in each iteration of the loop.

4) Then, the CAN.readMsgBuf() function is called to receive any messages on the CAN bus. If there is a message, it is stored in the recvmsg buffer. The received message is then printed to the serial monitor.

5) The loop is delayed by 1000 milliseconds before sending the next message. The process repeats continuously.

6) In this specific code, the recvmsg buffer is checked for specific values and the corresponding character is printed to the serial monitor. If the value in the recvmsg buffer is 65, "A" is printed, if the value is 67, "C" is printed, and if the value is 75, "K received" is printed.

# Receiver Code Explanation:
1) This code demonstrates the use of the MCP2515 library to enable communication between two Arduino boards via a CAN bus. The code begins with the definition of the SPI chip select (CS) pin and the CAN interrupt pin. The MCP2515_CAN object is then created with the specified CS pin.

2) The setup() function initializes the serial port and attaches an interrupt to the CAN interrupt pin. The CAN bus is then initialized with a baud rate of 500 kbps. The function waits until the initialization is successful before continuing.

3) The loop() function first checks if a flag flagRecv has been set to 1, indicating that a message has been received. If a message has been received, the flag is cleared and the function iterates over all pending messages using CAN.checkReceive(). The CAN.readMsgBuf() function is then used to read the length and data of the message into the len and buf variables.

4) The message is acknowledged using CAN.sendMsgBuf() with the ack message buffer. The message data is then printed to the serial monitor using a for loop.

5) The interrupt service routine MCP2515_ISR() is used to set the flagRecv flag to 1 when a message is received. This ISR is called when a falling edge is detected on the CAN interrupt pin.

6) Overall, the code demonstrates how to set up communication between two Arduino boards using a CAN bus and the MCP2515 library. The code reads messages from the bus and prints them to the serial monitor, and also sends a response message to acknowledge receipt of the original message.

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


