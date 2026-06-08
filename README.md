# Hardware / Robotics Systems Portfolio Website

This repository contains a personal hardware and robotics systems portfolio website.

The website summarizes hands-on project experience in robot hardware design, electrical and power system integration, STM32-based control firmware, motor control, hardware debugging, mechanical prototyping, and system-level validation.

---

## Overview

This portfolio focuses on practical engineering experience across hardware, electrical, mechanical, and control system implementation.

It includes two main projects:

1. AI-Based Smart Recycling Using 3-axis Orthogonal Coordinate Robot System Development
2. Towing AMR Hardware & Control System

The website is built as a static HTML/CSS/JavaScript page and is hosted through GitHub Pages.

---

## Main Features

- Single-page portfolio website
- Korean / English language toggle
- Project-based structure
- Problem → Decision → Solution → Result format
- Hardware, electrical, mechanical, and control system documentation
- Image, video, PDF, and GitHub code links
- Print / Save as PDF button
- Responsive layout for desktop and mobile

---

## Project 01 — AI-Based Smart Recycling Using 3-axis Orthogonal Coordinate Robot System Development

This project is an automatic sorting and ultrasonic cleaning system built with STM32-based control, motor driving, AC/DC power separation, and mechanical system integration.

The project includes motor control, power distribution design, circuit documentation, hardware debugging, 3-axis robot structure implementation, and system-level testing.

### Key Technical Elements

- STM32-based control firmware
- C programming
- Timer-based PWM motor control
- Encoder-based speed measurement
- PID control testing
- Relay-based AC 220V isolation control
- DC 24V to DC 12V / 5V power distribution design
- KiCad-based AC/DC circuit documentation
- Fusion 360-based mechanical and system modeling
- Hardware debugging based on actual circuit behavior

### Problem 1: Power Design Oversight

The step-down converter failed because the connected load exceeded its 5A current limit.

After comparing the damaged circuit with the original design calculations, the converter current limit and the actual PSU output limitation were identified.

The power distribution structure was redesigned based on the 5A converter limit and the actual PSU output of about 320W.

As a result, the power system became more stable, and the same failure did not recur.

### Problem 2: Encoder Sensor Failure

PID control was verified using a separate encoder motor.

However, the encoder sensor of the actual conveyor motor was faulty, so stable speed feedback could not be obtained from the real conveyor system.

The issue was determined to be a hardware sensor failure rather than a control algorithm problem.

The PID test result was documented as implementation evidence, and the actual conveyor system was switched to PWM control for stable operation.

### Evidence

- AC 220V circuit design PDF
- DC 24V to 12V / 5V power distribution PDF
- PID control GitHub repository
- Overall 3D modeling image
- Classification motion and 3-axis robot operation video
- PID control graph video
- Actual encoder motor PID control video

---

## Project 02 — Towing AMR Hardware & Control System

This project is a towing-capable AMR hardware platform with STM32-based control.

The project includes the full hardware and mechanical design of the towing robot, including the frame, lift structure, towing mechanism, motor control, and linear actuator-based lift control.

### Key Technical Elements

- STM32-based control firmware
- C programming
- PWM-based motor control
- Linear actuator-based lift control
- Fusion 360-based mechanical design
- Full towing robot hardware structure design
- Frame, lift, and towing mechanism fabrication
- 3D-printed part fabrication and assembly
- Repeated load testing and structural improvement
- Integration of mechanical structure and control system

### Key Contribution

The towing robot frame, lift mechanism, and towing structure were designed and fabricated directly.

The mechanical hardware was integrated with the control system to create a working hardware prototype.

This project demonstrates system-level engineering experience, including mechanical design, actuator control, hardware assembly, repeated testing, and structural improvement.

### Problem: Structural Stiffness and Durability

During repeated load testing, deformation occurred in the 3D-printed towing structure.

The towing geometry, fastening points, and load direction were analyzed to determine where structural reinforcement was needed.

The frame and towing structure were redesigned and improved through fabrication and repeated load testing.

As a result, a hardware structure capable of lift and towing operation was secured.

### Evidence

- AMR 3D design model image
- Towing robot operation diagram
- Prototype image without exterior cover
- Lift drive motion video
- Towing system operation video after improvement
- YouTube driving video link

---

## Technical Summary

### Control / Firmware

- STM32-based control firmware design
- Timer, PWM, and interrupt-based control structure
- Encoder speed measurement
- PID control implementation and testing
- Motor and actuator control logic implementation

### Electrical / Hardware

- AC/DC power separation design
- Power specification analysis and redesign
- DC power distribution design
- KiCad-based AC/DC circuit documentation
- Hardware debugging based on real circuit behavior
- Sensor, motor, actuator, and controller integration

### Mechanical / Prototyping

- Fusion 360-based mechanical design
- Frame, lift, and towing mechanism design
- 3D-printed part fabrication and assembly
- Mechanical structure improvement through repeated load testing
- Prototype assembly and validation

### System Integration

- Integration of firmware, electrical hardware, and mechanical structure
- Practical troubleshooting in real hardware environments
- Design decisions based on actual test results
- Iterative improvement from prototype testing

---

## Repository Structure

```text
youngmin-site/
├─ index.html
├─ README.md
└─ assets/
   ├─ img/
   │  ├─ project 1/
   │  │  ├─ RecyclingSystem-Power-Architecture-AC.pdf
   │  │  ├─ RecyclingSystem-Power-Architecture-DC.pdf
   │  │  └─ Overall Modelling.png
   │  │
   │  └─ project 2/
   │     ├─ AMR_3dfile.png
   │     ├─ Towing system image.PNG
   │     └─ Towing system image.jpeg
   │
   ├─ video/
   │  ├─ project 1/
   │  │  ├─ Classification motion images.MP4
   │  │  ├─ PID_Controll_100rpm.mp4
   │  │  └─ PID_MotorControll_realpart.mp4
   │  │
   │  └─ project 2/
   │     ├─ Towing system lift drive.MP4
   │     └─ Subsequent improvements in towing.MP4
   │
   └─ certificate-of-award/
      ├─ 240131 Capstone Design Encouragement Award Listed.jpg
      ├─ 20241122 Listed at the thesis contest.png
      ├─ 241203 Special Award for Capstone Design.jpg
      └─ 24 INTERFACE_WP245058_.jpg
