# 🚗 Autonomous Maze-Solving Robot Car

An autonomous robotic vehicle designed to navigate and solve mazes in real-time. Built using Arduino, this robot utilizes multiple ultrasonic sensors and control algorithms to detect walls, avoid obstacles, and find its way through complex paths.

## 🌟 Features
* **Real-time Obstacle Avoidance:** Uses 3 ultrasonic sensors (Front, Left, Right) to continuously monitor the surroundings.
* **Smart Navigation Logic:** Automatically adjusts its path if it gets too close to side walls and makes calculated turns when facing front obstacles.
* **PWM Motor Control:** Smooth speed adjustments using dual motor drivers.

## 🛠️ Hardware Components
* **Microcontroller:** Arduino Uno
* **Motor Driver:** L298N (or similar dual H-bridge motor driver)
* **Sensors:** 3x HC-SR04 Ultrasonic Sensors
* **Actuators:** DC Motors with wheels
* **Chassis:** 2WD/4WD Robot Chassis
* **Power:** Battery Pack
* Breadboard and Jumper Wires

## 🔌 Pin Configuration (Wiring)

### Motors
* `ENA` (Right Motor Speed) -> Pin 6
* `ENB` (Left Motor Speed) -> Pin 5
* `IN1` (Right Motor Dir) -> Pin 9
* `IN2` (Right Motor Dir) -> Pin 8
* `IN3` (Left Motor Dir) -> Pin 10
* `IN4` (Left Motor Dir) -> Pin 11

### Ultrasonic Sensors
* **Front Sensor:** Trig -> A0 | Echo -> A3
* **Left Sensor:** Trig -> A1 | Echo -> A4
* **Right Sensor:** Trig -> A2 | Echo -> A5

## 🚀 How It Works (Core Logic)
1. The robot moves forward by default.
2. It constantly measures the distance using the three ultrasonic sensors.
3. **Front Obstacle:** If an object is detected within 10 cm, it stops, compares the left and right distances, and turns towards the side with more space.
4. **Wall Alignment:** If the robot drifts too close to the left wall (< 8 cm), it slightly turns right to center itself, and vice versa.

## ⚙️ Setup and Installation
1. Clone this repository:
   ```bash
   git clone [https://github.com/ziadessam-debug/robot_maze_project.git](https://github.com/ziadessam-debug/robot_maze_project.git)
   
