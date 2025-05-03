# Hand-Following-Robot
Code in Ardunino IDE for hand following robot
you may have another pins connected to your Arduino, you can change them.
Obstacle Avoiding Robot using Arduino

This Arduino project controls a robot that detects and avoids obstacles using three ultrasonic sensors. It uses an L298N motor driver to move forward, turn, or stop based on the distance to nearby objects.

Overview
The robot:
- Moves **forward** if there is an obstacle **in front**.
- Turns **left** if there is an obstacle **on the left**.
- Turns **right** if there is an obstacle **on the right**.
- Stops if there are **no nearby obstacles**.

Components Used:
- Arduino Uno
- L298N Motor Driver Module
- 2 DC Motors
- 3x HC-SR04 Ultrasonic Sensors (Left, Right, Center)
- Jumper Wires
- Chassis + Wheels + Battery Pack

Pin Configuration:
Motor Driver
- `ENA` - Pin 3 (PWM)
- `ENB` - Pin 2 (PWM)
- `IN1` - Pin 4
- `IN2` - Pin 5
- `IN3` - Pin 6
- `IN4` - Pin 7

Ultrasonic Sensors:
- Left Sensor: `Trig` - Pin 10, `Echo` - Pin 11  
- Right Sensor: `Trig` - Pin 8, `Echo` - Pin 9  
- Center Sensor: `Trig` - Pin 12, `Echo` - Pin 13

Code Logic:
if (distanceCenter < 10)
    moveForward();
else if (distanceLeft < 10)
    turnLeft();
else if (distanceRight < 10)
    turnRight();
else
    stopMoving();
