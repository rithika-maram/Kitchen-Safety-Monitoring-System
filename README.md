# Kitchen Safety Heat and Gas Monitoring and Alert System

## 1. Project Overview

The **Kitchen Safety Heat and Gas Monitoring and Alert System** is an embedded systems project developed using the LPC2148 ARM7 microcontroller and Embedded C.

The system monitors kitchen temperature and gas levels using sensors. When the detected temperature or gas level exceeds a predefined threshold, the system provides an alert to help identify potentially unsafe conditions.

An LCD is used to display system information and sensor readings. A buzzer and LED indicators can provide alerts when configured threshold conditions are detected.

This project demonstrates the application of microcontrollers, sensor interfacing, ADC, LCD interfacing, and embedded C programming in a kitchen safety monitoring prototype.

## 2. Objectives

- Monitor kitchen temperature using the LM35 temperature sensor.
- Detect the presence of gas using the MQ-2 gas sensor.
- Display sensor readings and system status on an LCD.
- Generate alerts when configured temperature or gas thresholds are exceeded.
- Understand sensor interfacing and ADC-based data acquisition using the LPC2148 microcontroller.
- Develop practical skills in Embedded C programming and hardware interfacing.

## 3. Hardware Components

| Component | Purpose |
|---|---|
| LPC2148 ARM7 Development Board | Processes sensor readings and controls the system |
| LM35 Temperature Sensor | Measures temperature |
| MQ-2 Gas Sensor Module | Detects combustible gases and smoke-related changes |
| 16×2 LCD | Displays readings and system status |
| Buzzer | Provides an audible alert |
| LED Indicators | Indicate system status, if configured |
| Keypad | Provides user input, if implemented in the program |
| Connecting Wires | Connect the hardware components |
| Power Supply | Supplies power to the development board and interfacing circuits |

## 4. Software and Tools

- **Programming Language:** Embedded C
- **Microcontroller:** LPC2148 (ARM7-based)
- **IDE/Compiler:** Keil µVision
- **Hardware Testing:** LPC2148 development board
- **Simulation:** Proteus, if used in the project

## 5. Working Principle

1. The LPC2148 microcontroller initializes the required peripherals and connected devices.
2. The LM35 temperature sensor provides a voltage corresponding to the measured temperature.
3. The MQ-2 gas sensor module provides a signal that changes according to the detected gas concentration.
4. The microcontroller reads the sensor signals using the appropriate input interfaces. Analog signals are read through the ADC where applicable.
5. The measured values or system status are displayed on the LCD.
6. The sensor readings are compared with the configured threshold values.
7. When a threshold condition is detected, the corresponding alert is activated according to the implemented program.

**Note:** The MQ-2 sensor output should not be treated as an accurate gas concentration in ppm unless the sensor has been appropriately calibrated and the measurement method validated.

## 6. Hardware Setup and Output Images

The following images show the hardware setup and example outputs of the project.

### Hardware Overview

![Labeled hardware overview](./Labeled%20hardware%20overview.jpeg)

### Hardware Setup with Keypad

![Setup with keypad connected](./Setup%20with%20the%20keypad%20connected.jpeg)

### Temperature Alert

![Temperature alert output](./Temperature%20alert.jpeg)

### Gas Detection Outputs

**Gas Safe Condition**

![Gas safe condition](./Gas%20safe%20%28S0%29.jpeg)

**Gas Alert**

![Gas alert output](./Gas%20alert.jpeg)

**Gas Level Above Threshold**

![Gas above limit output](./Gas%20above%20limit%20%28S1%29.jpeg)

## 7. How to Run

1. Clone or download this repository.
2. Open the project source files in Keil µVision.
3. Confirm that the device configuration and required header files are correct for the LPC2148.
4. Build the project and resolve any compilation errors.
5. Connect the sensors, LCD, buzzer, and other peripherals according to the circuit connections defined in the source code.
6. Program the compiled output onto the LPC2148 development board using the appropriate programming utility.
7. Power on the board and observe the LCD readings and alert behavior under the supported test conditions.

**Note:** The exact build and programming steps depend on the project files and hardware configuration included in this repository.

## 8. Future Enhancements

- Add SMS or mobile notifications for detected unsafe conditions.
- Add data logging to record temperature and gas sensor readings.
- Improve sensor calibration and measurement accuracy.
- Add wireless monitoring using an appropriate communication module.
- Integrate a properly designed automatic gas shutoff mechanism, with suitable safety testing.

## 9. Applications

- Educational embedded systems projects
- Kitchen temperature and gas monitoring demonstrations
- Sensor interfacing and microcontroller learning
- Embedded C and ADC experimentation

## 10. Safety Disclaimer

This project is an educational prototype and is **not a certified kitchen safety or gas-leak prevention device**. It should not replace certified gas detectors, smoke alarms, or other approved safety equipment.

## 11. Author

**Project:** Kitchen Safety Heat and Gas Monitoring and Alert System  
**Platform:** LPC2148 ARM7 Microcontroller  
**Language:** Embedded C
