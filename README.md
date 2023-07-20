# Overview
This repository contains the firmware and software for a Capacitance-Based Moisture Detection System designed to measure the moisture content of surface sheets, such as drywall. The system utilizes two arrays of NE555 sensors, each with 16 sensors, totaling 32 sensors. By detecting changes in capacitance caused by the sheet's dielectric properties, the sensors generate pulse frequencies that correlate with the moisture levels. The captured data is transmitted via UDP to a Qt C++ application, which displays real-time moisture distribution on two 25x16 bitmaps.

### Features
High-precision moisture detection through NE555 sensors utilizing capacitance changes.
Fast data capture at a rate of 10ms for accurate and real-time moisture measurements.
UDP communication for seamless data transfer from the microcontroller to the Qt C++ application.
Qt software interface with two 25x16 bitmaps to visualize the moisture distribution on the surface sheet.
IR sensor for sheet arrival and movement detection, enabling efficient moisture data capture.

### Components
NE555 Sensors: A total of 32 NE555 sensors are distributed in two arrays of 16 sensors each.
Sheet Movement Mechanism: The system accommodates the movement of the surface sheet above the sensor arrays.
IR Sensor: Detects sheet arrival and movement to initiate moisture data capture.
Microcontroller STM32: Processes sensor data and controls data transmission to the software.
UDP Communication: Facilitates data transfer from the microcontroller to the Qt C++ application.
Qt C++ Application: Visualizes moisture data on two 25x16 bitmaps for real-time analysis.

## Setup and Usage

### Hardware Setup:
- Arrange the two arrays of NE555 sensors (16 sensors in each array) beneath the surface sheet.
- Install the IR sensor to detect sheet arrival and movement.
- Connect the sensors and IR sensor to the microcontroller.

### Firmware Setup:
- Flash the provided firmware onto the microcontroller STM32 using an appropriate tool.

### Software Setup:
- Install the required dependencies for the Qt C++ application.
- Compile and run the Qt software on the computer.

### User Interface:
- The Qt software displays real-time moisture data on two 25x16 bitmaps.
- The bitmaps represent the moisture distribution across the surface sheet.

### Moisture Detection:
- The IR sensor triggers the data capture process when a sheet arrives or moves.
- The microcontroller measures changes in capacitance using the NE555 sensors.
- Two matrices (25x16) are created with the captured moisture data.
- The data is sent via UDP to the Qt C++ application for visualization.

## Contribution Guidelines
Contributions to the Capacitance-Based Moisture Detection System are welcome! If you wish to contribute, please follow these guidelines:

Fork the repository and create a new branch for your feature or bug fix.
Make your changes, test them thoroughly, and ensure the code adheres to the project's coding standards.
Commit your changes and create a detailed pull request with a clear explanation of the changes and their purpose.

## Licensing
The Capacitance-Based Moisture Detection System is licensed under the [MIT License](https://github.com/AmirhoseinMasoumi/MoistureDetection/blob/main/LICENSE).

## Disclaimer
This Capacitance-Based Moisture Detection System is intended for informational purposes only. The developers and maintainers of this repository are not responsible for any direct or indirect damages caused by the use or misuse of the system.
