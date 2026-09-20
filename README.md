
# Logic-Based Maze-Solving Robot 🤖

A maze-navigation robot designed using digital logic ICs, IR sensors, and a TB6612FNG motor driver, without using a microcontroller.

## 📌 Project Overview

This project demonstrates how a robot can make navigation decisions using combinational logic instead of software-based control.

Three IR sensors detect obstacles in the front, left, and right directions. The logic circuit processes these signals and controls four DC gear motors.

## 🛠️ Hardware Components

| Component | Purpose |
|---|---|
| 3 × IR sensors | Obstacle detection |
| 74HC14 | Signal inversion |
| 74LS08 | AND logic |
| 74HC11 | Three-input AND logic |
| 74HC32 | OR logic |
| TB6612FNG | Dual motor driver |
| 4 × DC gear motors | Robot movement |
| 18650 Li-ion batteries | Power source |
| LM2596 buck converter | Regulated 5V supply |

## 🧠 Navigation Logic

The robot follows a priority-based navigation strategy:

1. Front clear → Move forward
2. Front blocked, left clear → Turn left
3. Front and left blocked, right clear → Turn right
4. All directions blocked → Stop

The IR sensors provide active-low obstacle detection signals.

## ⚙️ Motor Control

The TB6612FNG controls the left and right motor groups.

| Movement | AIN1 | AIN2 | BIN1 | BIN2 |
|---|---|---|---|---|
| Forward | HIGH | LOW | HIGH | LOW |
| Left | LOW | HIGH | HIGH | LOW |
| Right | HIGH | LOW | LOW | HIGH |
| Stop | LOW | LOW | LOW | LOW |

Motor-driver standby and PWM inputs must also be enabled for movement.

## 🔋 Power System

The system uses Li-ion batteries for the motors and an LM2596 buck converter for the regulated logic supply.

## 🧪 Implementation and Testing

The control circuit was assembled and tested on the bench. Motor-direction control and logic-based navigation decisions were verified during development.

Full maze-navigation performance is not documented here.

## 📸 Circuit Diagram and Hardware

Circuit diagrams, hardware photographs, and available testing evidence will be added to this repository.

## 🎯 Learning Outcomes

- Combinational logic design
- IR sensor interfacing
- DC motor control
- Power regulation
- Hardware troubleshooting
- Logic-based robotic navigation

## 👨‍💻 Author

**Md. Shahriar Alam Rivon**

Electrical & Electronic Engineering  
East West University, Bangladesh

[GitHub](https://github.com/shahriaralam-rivon) | [LinkedIn](https://www.linkedin.com/in/md-shahriar-alam-rivon-4449aa410/)
