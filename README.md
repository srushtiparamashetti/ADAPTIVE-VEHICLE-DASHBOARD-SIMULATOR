# ADAPTIVE-VEHICLE-DASHBOARD-SIMULATOR
ADAPTIVE-VEHICLE-DASHBOARD-SIMULATOR
An LPC2129-based adaptive vehicle dashboard simulator that monitors vehicle parameters such as speed, fuel level, temperature, and indicator status, and transfers real-time data between two microcontroller nodes using CAN communication.

# Project Overview
This project is an embedded systems-based vehicle dashboard simulation using two LPC2129 ARM7 microcontroller nodes. It monitors vehicle speed using a potentiometer, fuel level using an ultrasonic sensor, and temperature using an LM35 sensor. It also handles vehicle indicator information, including left indicator, right indicator, and headlight status.

The sensor readings and indicator information are collected at Node A (Transmitter) and transmitted to Node B (Receiver) through the CAN protocol using interrupt-based communication. The received data is processed and displayed on the serial monitor using UART communication.

# Key Features
Vehicle speed monitoring using a potentiometer.   
Fuel level monitoring using an ultrasonic sensor.   
Engine temperature monitoring using an LM35 sensor.    
Left indicator status detection.   
Right indicator status detection.    
Headlight status detection.    
ADC-based analog sensor data acquisition.  
External interrupt handling for indicator inputs.   
CAN interrupt-based data transmission and reception.   
UART-based real-time dashboard monitoring.    
Data packing and unpacking using bitwise operations.   
# Hardware Components
LPC2129 ARM7 Microcontrollers (2)  
Potentiometer for speed simulation  
Ultrasonic sensor for fuel level monitoring  
LM35 temperature sensor   
Indicator switches (Left and Right)  
Headlight switch   
CAN communication interface  
UART serial communication interface  
# Software and Tools
Embedded C  
Keil µVision IDE  
ADC  
GPIO  
External Interrupts (EINT)  
CAN Protocol  
CAN Interrupts  
UART Protocol  
Serial Monitor  
# System Architecture
# Node A – Transmitter
Reads vehicle speed using a potentiometer through ADC.   
Measures fuel level using an ultrasonic sensor.   
Reads temperature using the LM35 sensor through ADC.  
Detects left indicator, right indicator, and headlight status using external interrupts/GPIO inputs.  
Packs the sensor readings and indicator information into a CAN data frame.   
Transmits vehicle information to Node B using CAN communication.   
Uses interrupt-based CAN communication for data transfer.   
# Node B – Receiver
Receives vehicle information from Node A through CAN communication.   
Handles CAN data reception using interrupts.   
Extracts individual sensor values and indicator status using bitwise operations.   
Processes the received data to obtain meaningful vehicle parameters.   
Displays speed, fuel level, temperature, left indicator, right indicator, and headlight status on the serial monitor using UART communication. 
# Communication Protocols
Protocol	Purpose
ADC	Potentiometer and LM35 sensor data acquisition  
GPIO	Digital input and output control   
External Interrupts	Detecting indicator and headlight input events  
CAN	Communication between Node A and Node B   
CAN Interrupts	Interrupt-based CAN data transmission and reception  
UART	Displaying received dashboard information on the serial monitor   
# Working Principle
Node A collects vehicle speed, fuel level, and temperature readings from the respective sensors.  
Indicator and headlight information is detected through digital inputs and external interrupt handling.    
All collected information is packed into a CAN data frame.  
Node A transmits the CAN frame to Node B.    
Node B receives the CAN frame through interrupt-based CAN communication.   
The received data is unpacked and processed using bitwise operations.   
The final vehicle parameters and indicator statuses are displayed on the serial monitor using UART.    
# Learning Outcomes
LPC2129 ARM7 microcontroller programming. 
ADC and GPIO peripheral interfacing.   
Potentiometer, ultrasonic, and LM35 sensor interfacing.  
External interrupt configuration and handling.   
CAN protocol configuration and interrupt-based communication.    
CAN data frame packing and unpacking.    
UART serial communication.   
Multi-node embedded system design.   
Real-time vehicle parameter monitoring.    
# Applications
Automotive dashboard simulation.   
Vehicle parameter monitoring systems.  
Embedded automotive communication systems.   
CAN-based distributed control systems.    
Automotive electronics prototyping.   
# Future Scope
Integrating an OLED or LCD dashboard display.   
Adding warning alerts for low fuel and high temperature.  
Implementing automatic indicator switching.   
Adding vehicle speed-based adaptive alerts.   
Integrating wireless monitoring through Bluetooth or Wi-Fi.   
Extending the system to support additional vehicle parameters.   
# Disclaimer
This project is developed for educational and simulation purposes. It demonstrates vehicle parameter monitoring and CAN-based communication between microcontroller nodes. It is not intended for direct use in real vehicle control or safety-critical automotive applications.
