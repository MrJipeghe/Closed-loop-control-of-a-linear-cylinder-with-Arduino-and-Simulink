# Closed-Loop Control of a Pneumatic Linear Cylinder with Arduino and Simulink

This project demonstrates the implementation of a closed-loop control system for a pneumatic linear cylinder using an Arduino Leonardo and Simulink. The objective was to control the position of the cylinder accurately by processing feedback from a potentiometer and controlling an ON/OFF solenoid valve through a relay.

## Project Overview

The system uses Simulink as the main control interface, which sends commands to the Arduino. The Arduino reads the position of the cylinder via an analog signal from the potentiometer and controls the valve accordingly to reach the desired position.

## Components Used

- Pneumatic linear cylinder with integrated potentiometer
- ON/OFF solenoid valve (electrically actuated)
- Relay module for valve control
- Arduino Leonardo microcontroller
- Simulink (for real-time control and programming)
- 5V power supply for the valve
- USB power for Arduino
- Pneumatic tubing, compressor, and pressure regulator

## System Description

### Open-Loop Control

An initial test was conducted using open-loop control. A fixed signal from Simulink commanded the valve to open for a defined duration (5 seconds), resulting in full extension or retraction of the cylinder.

### Closed-Loop Control

Closed-loop control was then implemented using feedback from the potentiometer. Simulink transmitted a desired position, and the Arduino controlled the valve to move the cylinder toward that position. The system successfully demonstrated basic position control, but exhibited oscillations near the target position.

## Observed Issues

- Visible oscillations around the target position
- Delayed response due to pneumatic inertia
- Insufficient valve voltage (only 5V used)
- Relay powered directly from Arduino, leading to switching instability

## Proposed Solutions

- Replace ON/OFF valve with a proportional pneumatic valve for smoother control
- Increase valve supply voltage to 12V or 24V, as per specifications
- Use a transistor circuit to separate relay power from the Arduino
- Implement discrete PID control in Simulink
- Fine-tune air pressure using a pressure regulator
- Add pneumatic dampers at the stroke limits to reduce recoil

## Conclusion

The project successfully demonstrated the concept of electronically controlling a pneumatic actuator in both open-loop and closed-loop configurations. The results highlighted the limitations of basic components and pointed to possible improvements using better control strategies and hardware upgrades.

## Authors

- Birgiszer Roland  
- Hotea Alexandra  
- Group 30133, Year 2024–2025  
- Faculty of Automation and Computer Science, Romanian Section
