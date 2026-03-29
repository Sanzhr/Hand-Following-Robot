# Hand-Following Mobile Robot

## Description
This project presents a mobile robot that follows a human hand using distance measurements from ultrasonic sensors.

The robot detects the relative position of a hand (left, center, right) and adjusts its movement accordingly in real time.

## Features
- Real-time hand tracking using ultrasonic sensors
- Direction-based motion control (left, right, forward)
- Simple human-robot interaction system
- Motor control using L298N driver

## How It Works
The robot uses three ultrasonic sensors (left, center, right) to detect the position of a hand:

- If the hand is detected in front → the robot moves forward
- If the hand is detected on the left → the robot turns left
- If the hand is detected on the right → the robot turns right
- If no hand is detected → the robot stops

This creates a simple hand-following behavior.

## Hardware Components
- Arduino Uno
- L298N motor driver
- 2 DC motors
- 3x HC-SR04 ultrasonic sensors
- Chassis + wheels + battery

## Pin Configuration

### Motor Driver
- ENA → Pin 3
- ENB → Pin 2
- IN1 → Pin 4
- IN2 → Pin 5
- IN3 → Pin 6
- IN4 → Pin 7

### Ultrasonic Sensors
- Left: Trig → Pin 10, Echo → Pin 11
- Right: Trig → Pin 8, Echo → Pin 9
- Center: Trig → Pin 12, Echo → Pin 13

## Technologies Used
- Arduino IDE
- Embedded C/C++
- Ultrasonic sensing
- Real-time control logic

## Project Goal
The goal of this project was to explore basic human-robot interaction and sensor-based control for mobile robotics systems.
