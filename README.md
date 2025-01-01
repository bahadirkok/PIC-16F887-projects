# PIC-16F887-projects

Project Description
This project implements a line-following robot using a PIC16F887 microcontroller. The robot detects the line with two TCRT5000 infrared sensors and controls the motors via an L298N motor driver.

Hardware Connections
Sensors:
TCRT5000 Sensor 1 (Left): RA0 (Digital Input)
TCRT5000 Sensor 2 (Right): RA1 (Digital Input)
L298N Motor Driver:
Left Motor Control:
IN1: RC3 (Forward)
IN2: RC4 (Backward)
Enable1: RC1 (PWM)
Right Motor Control:
IN3: RC5 (Forward)
IN4: RC6 (Backward)
Enable2: RC2 (PWM)
Software Features
Sensor Reading:
Reads digital signals from the sensors to detect the line position.

Motor Control:
Controls the direction and speed of both motors:

Left motor: RC3 and RC4
Right motor: RC5 and RC6
Speed control via PWM on RC1 and RC2.
Logic:

Both sensors detect black (on the line): Robot stops.
Left sensor white, right sensor black: Turns right.
Right sensor white, left sensor black: Turns left.
Both sensors detect white (off the line): Moves forward.
PWM Control:
Uses a fixed duty cycle (127) for motor speed.

Requirements
Microcontroller: PIC16F887
Motor Driver: L298N
Sensors: 2x TCRT5000
Compiler: MPLAB XC8 or equivalent
Usage
Connect the hardware as described above.
Compile the code and upload it to the PIC16F887.
Test the robot on a white surface with a black line.
The code is configured for an 8 MHz external oscillator. Adjust the oscillator settings if necessary.

Proteus scheme:
![Ekran görüntüsü 2024-12-28 000928](https://github.com/user-attachments/assets/551d62dd-5f1e-4948-a076-796e3e6027c4)
