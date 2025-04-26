# Writing-Machine-Arduino-CNC
This Project is shared with whom is interested to build his own writing machine, the machine is based on Arduino Uno and CNC shield, a full description is included.

# DPI Writing Machine

This repository contains the design files, Arduino software, and instructions for building and operating a DPI writing machine. The machine uses a servo-controlled pen plotter mechanism to write precise text or drawings on various surfaces.

## Overview

The DPI writing machine is a pen plotter driven by Arduino, capable of creating detailed plots and writing text by controlling servo motors and stepper motors to move the pen across a two-dimensional plane.

## Mechanical Design

### Components Required:

- Arduino Uno (or similar microcontroller)
- Servo motor (for pen lifting and lowering)
- Stepper motors (x2, for X and Y axis control)
- Stepper motor drivers (A4988 or DRV8825 recommended)
- Linear rails and bearings for smooth axis movement
- Timing belts and pulleys
- Pen holder mechanism
- Frame (3D printed or aluminum extrusion recommended)

### Assembly Process:

1. **Frame Construction**: Assemble the base frame using aluminum extrusion or a rigid structure to ensure stability.
2. **Axis Setup**: Mount linear rails, bearings, and timing belts for precise motion along X and Y axes.
3. **Stepper Motor Installation**: Secure stepper motors and connect them via timing belts and pulleys to the moving axis carriages.
4. **Servo Pen Mechanism**: Attach a servo motor with a pen holder designed to lift and lower the pen as needed during plotting.

## Electronics & Wiring

- Connect stepper motors to respective drivers and Arduino pins according to provided wiring diagrams.
- Connect the servo motor for pen control directly to the Arduino PWM pin.
- Ensure proper power supply (12V recommended for motors, 5V for Arduino).

## Software

### Arduino Code
- The Arduino sketch provided controls the movement of stepper motors and the servo motor for precise writing.
- Movement commands follow standard G-code formatting, facilitating ease of plotting various designs.
- Servo positions:
  - `M3 S0`: Pen up
  - `M3 S90`: Pen down (writing position)

### Required Software

- **Arduino IDE**: For uploading and modifying the Arduino sketch.
- **Universal G-code Sender (UGS)** or similar software: Used for sending G-code commands to the Arduino.

## Operating Instructions

1. Upload the provided Arduino sketch to the microcontroller.
2. Generate or prepare your G-code plot file using Inkscape or a similar tool.
3. Connect your machine to a computer and launch UGS or equivalent software.
4. Load your G-code file into the sender application and start plotting.

## License

This project is open source and licensed under the MIT License. Contributions and improvements are welcome!


