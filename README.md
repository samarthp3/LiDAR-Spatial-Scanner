# LiDAR-Spatial-Scanner
This repository contains the files for a Integrated LiDAR Spatial Mapping Scanner

FULL DETAILED REPORT (including set-up guide and device specifications) AVAILABLE ON REQUEST

**ABOUT**

The ILRSK is a kit which uses LiDAR to scan and map a 3-D visual of a room. It contains a variety of easily accessible components. The core component of the kit is the Texas Instrument MSP432E401Y Microcontroller. This device works with 1 external push button, a breadboard, and a VL53L1X Time of Flight (ToF) sensor mounted to the 28BYJ-48 with a ULN2003 driver to rotate 360° and capture data for a series of y-z planes one at a time. A script is then used to conjoin the planes and generate a 3D visual of the room.

The entire system is connected to a PC which executes two python scripts for data acquisition and 3D model visualization. While running the data collection file, the ToF collects and transmits data via emitting a beam of light and keeping track travel time. It then uses the ADC process to obtain discrete values, which then is used to calculate object/target distance. This data, including distance, displacement, and angle, is sent to the microcontroller via I2C. This data is then transmitted via UART from the microcontroller to the PC. The scripts then convert the data into x, y, and z values which is then stored and used by the second script for 3D visualization.

Below is an image of the key devices used in this project

![image](https://github.com/samarthp3/LiDAR-Spatial-Scanner/assets/113307694/348f2d38-eb5d-47d2-8d0e-77533167db9d)

**FEATURES**

• Live data readings from ToF sensor to the microcontroller via I2C communication

• Live data transmission from Microcontroller to PC via UART communication at 115200 BPS (bits per second) baud rate

• 12 MHz clock speed operation

• On-board LED measurement (PN1) and data transmission status (PF4)

• Input voltage supply range from 3.3V to 5V

• 1-push button user interface to enable both rotation and the data acquisition process

• Automated 3D plot generation using Python IDLE and Open3D

• VL53L1X Time-of-Flight Sensor

    o Measure up to a 4m range
    
    o 2.6V – 3.5V range of operating voltage
    
    o 16-bit I2C distance readings (in mm)
    
• 28BYJ-48 Stepper Motor

    o 5V – 12V range of operating voltage

![image](https://github.com/samarthp3/LiDAR-Spatial-Scanner/assets/113307694/8c81d9ab-ef48-4dcc-8e51-23c6bef6e13c)

