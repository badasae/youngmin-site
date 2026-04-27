# Embedded Portfolio Website

This repository contains a personal embedded systems portfolio website.

The website summarizes hands-on project experience in STM32 firmware development, motor control, power distribution design, hardware debugging, and mechanical prototyping.

---

## Overview

This portfolio focuses on embedded system development with real hardware implementation.

It includes two main projects:

1. AI-Based Smart Recycling Using 3-axis Orthogonal Coordinate Robot System Development
2. Towing AMR Embedded Control System

The website is built as a static HTML/CSS/JavaScript page and is hosted through GitHub Pages.

---

## Main Features

- Single-page portfolio website
- Korean / English language toggle
- Project-based structure
- Problem → Decision → Solution → Result format
- Embedded firmware and hardware project documentation
- Image, video, PDF, and GitHub code links
- Print / Save as PDF button
- Responsive layout for desktop and mobile

---

## Project 01 — AI-Based Smart Recycling Using 3-axis Orthogonal Coordinate Robot System Development

This project is an STM32-based automatic sorting and ultrasonic cleaning system.

The project includes motor control, AC/DC power separation, power distribution design, circuit documentation, and hardware debugging.

### Key Technical Elements

- STM32 firmware development
- C programming
- Timer-based PWM control
- Encoder-based speed measurement
- PID control testing
- Relay-based AC 220V isolation control
- DC 24V to DC 12V power distribution design
- KiCad-based AC/DC circuit documentation
- Fusion 360-based system modeling

### Problem 1: Power Design Oversight

The step-down converter failed because the load exceeded its 5A current limit.

After comparing the damaged circuit with the original design calculations, the converter current limit and actual PSU output limitation were identified.

The power distribution structure was redesigned based on the 5A converter limit and the actual PSU output of about 320W.

### Problem 2: Encoder Sensor Failure

PID control was verified using a separate encoder motor.

However, the encoder sensor of the actual conveyor motor was faulty, so stable speed feedback could not be obtained.

The PID test result was documented as evidence, and the actual conveyor system was switched to PWM control for stable operation.

### Evidence

- AC circuit design PDF
- DC circuit design PDF
- PID control GitHub repository
- PID control graph video
- Actual encoder motor PID control video

---

## Project 02 — Towing AMR Embedded Control System

This project is a towing-capable AMR hardware platform with STM32-based control.

The project includes the full hardware and mechanical design of the towing robot, including the frame, lift structure, and towing mechanism.

### Key Technical Elements

- STM32 firmware development
- C programming
- PWM-based motor control
- Linear actuator-based lift control
- Fusion 360-based mechanical design
- Full towing robot hardware structure design
- Frame, lift, and towing mechanism fabrication
- 3D-printed part fabrication and assembly
- Repeated load testing and structural improvement

### Key Contribution

The towing robot frame, lift mechanism, and towing structure were designed and fabricated directly.

The mechanical hardware was integrated with the control system to create a working hardware prototype.

### Problem: Structural Stiffness and Durability

During repeated load testing, deformation occurred in the 3D-printed towing structure.

The towing geometry, fastening points, and load direction were analyzed to determine where structural reinforcement was needed.

The frame and towing structure were redesigned and improved through fabrication and repeated load testing.

### Evidence

- AMR 3D design model image
- Towing robot operation diagram
- Prototype image without exterior cover
- Lift drive motion video
- Towing system operation video after improvement
- YouTube driving video link

---

## Technical Summary

### Firmware

- STM32 firmware design
- Timer, PWM, and interrupt-based control structure
- Encoder speed measurement
- PID control implementation and testing

### Power & Hardware

- AC/DC power separation design
- Power specification analysis and redesign
- KiCad-based AC/DC circuit documentation
- Hardware debugging based on real circuit behavior

### Mechanical

- Fusion 360-based mechanical design
- Frame, lift, and towing mechanism design
- 3D-printed part fabrication and assembly
- Structural improvement through repeated load testing

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
   │  │  └─ RecyclingSystem-Power-Architecture-DC.pdf
   │  └─ project 2/
   │     ├─ AMR_3dfile.png
   │     ├─ Towing system image.PNG
   │     └─ Towing system image.jpeg
   │
   ├─ video/
   │  ├─ project 1/
   │  │  ├─ PID_Controll_100rpm.mp4
   │  │  └─ PID_MotorControll_realpart.mp4
   │  └─ project 2/
   │     ├─ Towing system lift drive.MP4
   │     └─ Subsequent improvements in towing.MP4
   │
   └─ certificate-of-award/
      ├─ 240131 Capstone Design Encouragement Award Listed.jpg
      ├─ 20241122 Listed at the thesis contest.png
      ├─ 241203 Special Award for Capstone Design.jpg
      └─ 24 INTERFACE_WP245058_.jpg
```

---

## External Links

### PID Control Code

The PID control code is managed in a separate GitHub repository.

```text
https://github.com/badasae/STM32_MotorControll_PID/tree/main
```

### Towing System Driving Video

```text
https://youtu.be/PHcA-O1GWsk
```

---

## Notes

This website is intended to present embedded system project experience through actual implementation evidence.

The main focus is not only on writing firmware code, but also on solving real hardware problems such as power instability, sensor failure, mechanical deformation, and system integration issues.

The portfolio demonstrates practical engineering decision-making in real project conditions.
