# Kitchen Safety Heat and Gas Monitoring and Alert System

An ARM7-based embedded systems project using the LPC2148 microcontroller to monitor kitchen temperature and gas sensor readings and provide alerts when configured safety thresholds are exceeded.

## 📌 Project Overview

Kitchen environments can be exposed to excessive heat and gas leakage. This project implements an embedded monitoring system that continuously reads temperature and gas sensor values, displays system information on an LCD, and activates an alert when a configured threshold is crossed.

The system is developed using the LPC2148 ARM7 microcontroller and Embedded C. It combines sensor interfacing, ADC, LCD interfacing, keypad input, RTC functionality, and interrupt-based user interaction.

## 🎯 Objectives

- Monitor temperature using the LM35 temperature sensor.
- Read gas sensor output from the MQ-2 sensor through the ADC.
- Display temperature, gas readings, date, time, and system status on an LCD.
- Generate audible and visual alerts when configured limits are exceeded.
- Provide password-protected access to system settings.
- Allow users to configure temperature and gas thresholds.
- Record alert-related readings and timestamps for monitoring.

## 🛠️ Hardware Components

| Component | Purpose |
|---|---|
| LPC2148 ARM7 Microcontroller | Main controller |
| LM35 Temperature Sensor | Temperature measurement |
| MQ-2 Gas Sensor | Gas/smoke-related sensor readings |
| 16×2 LCD | Displaying readings and system messages |
| 4×4 Matrix Keypad | User input and settings |
| RTC | Date and time information |
| Buzzer | Audible alert |
| LED | Visual alert |
| Push Buttons / Switches | User interaction and alert control |

## 💻 Software and Tools

- Embedded C
- Keil µVision IDE
- Proteus Design Suite for circuit simulation
- Flash Magic for programming the microcontroller, if used

## ⚙️ System Architecture

The system follows this general operating sequence:

1. Initialize the microcontroller peripherals, LCD, ADC, keypad, and RTC.
2. Read temperature from the LM35 sensor.
3. Acquire the MQ-2 sensor output through the ADC.
4. Display the readings and relevant system information on the LCD.
5. Compare the sensor readings with the configured safety limits.
6. Activate the buzzer and LED when a threshold is exceeded.
7. Allow authorized access to configuration settings through password verification.
8. Store and display relevant alert information, including the reading and timestamp, as implemented in the program.

## 🔄 Working Principle

### 1. Temperature Monitoring

The LM35 provides an analog output corresponding to temperature. The LPC2148 ADC reads the sensor signal, and the program processes the reading for display and threshold comparison.

### 2. Gas Monitoring

The MQ-2 sensor provides an output that is read through the microcontroller's ADC. The program checks the resulting ADC reading against a configured limit and generates an alert when the limit is exceeded.

**Note:** The MQ-2 reading is treated as an ADC value in this implementation. It should not be interpreted as a calibrated gas concentration in ppm.

### 3. LCD Display

The LCD displays sensor readings, date and time information, alerts, and menu prompts to help the user monitor the system.

### 4. Alert Mechanism

When the temperature or gas reading crosses its configured threshold, the system activates the buzzer and LED to notify the user.

### 5. Password-Protected Settings

The keypad and switch-based interface provides access to protected settings. The implemented menu supports configuring safety thresholds and the password, with a lockout mechanism after repeated incorrect password attempts.

### 6. Event Monitoring

The program records relevant alert information, such as sensor readings and timestamps, and can display the latest recorded event.

## 🔐 Security and Configuration

The implemented interface includes:

- Password verification before accessing protected settings.
- Configurable temperature and gas thresholds.
- Password-change functionality.
- A temporary lockout after repeated incorrect attempts.
- User control for temporarily silencing the alarm.

The available settings and timeout behavior depend on the final program configuration.

## 📁 Repository Structure

```text
Kitchen-Safety-Monitoring-System/
│
├── README.md
├── main.c
├── types.h
├── defines.h
├── delay.c
├── delay.h
├── LCD.c
├── LCD.h
├── LCD_defines.h
├── KPM.c
├── KPM.h
├── KPM_defines.h
├── LM35.c
├── LM35.h
├── ADC.c
├── ADC.h
├── RTC.c
├── RTC.h
├── pin_connect_block.c
├── pin_connect_block.h
│
├── Circuit_Diagram/
├── Proteus_Simulation/
└── Output_Images/
```

*The file list above is illustrative. Keep the filenames that actually exist in your project, and add the other driver files required by your code.*

## ▶️ Build and Run Instructions

1. Open the Keil µVision project, if a project file is available.
2. Verify the target microcontroller and project configuration.
3. Add or confirm all required source and header files.
4. Check the GPIO pin assignments, ADC configuration, LCD connections, keypad connections, and RTC setup.
5. Build the project and resolve any compilation errors.
6. Program the LPC2148 board using the appropriate programming procedure, or load the program into the supported simulation setup.
7. Verify the LCD output, sensor readings, threshold alerts, keypad operation, and event display.

## 🧪 Testing

The following tests can be documented with your actual hardware or simulation results:

- LCD initialization and display.
- Temperature sensor reading and display.
- Gas sensor ADC reading and display.
- Temperature threshold alert.
- Gas threshold alert.
- Password verification and incorrect-attempt handling.
- Configuration menu operation.
- RTC date and time display.
- Alert event recording and display.
- Buzzer and LED response.

Add screenshots or photographs to demonstrate the tests you have actually completed.

## 🚀 Future Enhancements

- Add remote notifications for gas or temperature alerts.
- Integrate a calibrated gas measurement system.
- Add non-volatile storage for configuration settings and event records.
- Integrate a certified gas shutoff mechanism where appropriate.
- Improve the user interface and add additional diagnostic information.

These are proposed enhancements and are not claimed as completed features.

## 📚 Concepts Demonstrated

- ARM7 LPC2148 microcontroller programming
- Embedded C programming
- Analog-to-Digital Conversion (ADC)
- Sensor interfacing
- LCD and keypad interfacing
- Real-Time Clock (RTC)
- Interrupt handling
- Threshold-based monitoring
- Embedded system debugging and simulation

## 👩‍💻 Author

**Maram Rithika**

B.Tech – Electronics and Communication Engineering

Project Domain: Embedded Systems

## ⚠️ Disclaimer

This is an educational embedded systems project. It is not a certified kitchen safety device. The sensor readings and alert behavior depend on the hardware, calibration, and software implementation. Do not rely on this prototype as the sole protection against gas leakage or fire.
