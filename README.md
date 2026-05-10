# PWM Based Speed Control of DC Motor using Arduino

This project implements a **PWM (Pulse Width Modulation) based DC motor speed control system** using an **Arduino UNO** and an **L298N H-Bridge motor driver**. Motor speed is controlled by varying PWM duty cycle using a **potentiometer**, motor direction is selected via **push buttons**, and a **16×2 LCD** displays real-time speed percentage and direction.

![Hardware prototype](./assets/hardware-model-photo.png)

<!-- Fallback for some markdown renderers -->
<p>
  <img src="./assets/hardware-model-photo.png" alt="Hardware prototype" width="800" />
</p>

## Features

- **Smooth speed control** using PWM duty-cycle adjustment
- **Bidirectional rotation** using H-Bridge direction control (Clockwise / Anticlockwise)
- **Real-time LCD status**: speed (%) and direction
- **Efficient control** compared to conventional series voltage-drop methods

## Objectives

- Control DC motor speed using PWM technique
- Implement efficient motor drive control using Arduino UNO
- Generate variable PWM signals for speed regulation
- Control motor direction using H-Bridge driver circuitry
- Display real-time speed and direction on a 16×2 LCD
- Provide user-friendly speed control using a potentiometer
- Improve efficiency compared to conventional voltage control methods
- Understand practical applications of embedded motor control systems

## Components (Hardware)

- Arduino UNO
- L298N motor driver module (H-Bridge)
- DC motor
- Potentiometer (speed setpoint)
- Push buttons (direction / control)
- 16×2 LCD display
- Power supply (as required by motor + driver)
- Connecting wires, breadboard/perfboard, etc.

## How it works

1. The **potentiometer** provides an analog voltage to the Arduino.
2. The Arduino maps this value to a **PWM duty cycle** and outputs PWM on a motor control pin.
3. The **L298N driver** switches motor supply according to the PWM input and direction inputs.
4. The **LCD** continuously displays:
   - Speed as a percentage (based on duty cycle)
   - Rotation direction (Clockwise / Anticlockwise)

## Mathematical basis (PWM)

PWM controls the **effective (average) voltage** applied to the motor by rapidly switching the supply ON/OFF at high frequency.

### Average output voltage

\[
V_{\text{avg}} = D \times V_s
\]

Where:
- \(V_{\text{avg}}\): average motor voltage  
- \(D\): PWM duty cycle (0 to 1)  
- \(V_s\): supply voltage  

As duty cycle increases, \(V_{\text{avg}}\) increases, so motor speed increases.

### Duty cycle

\[
D(\%) = \frac{T_{\text{ON}}}{T} \times 100
\]

Where:
- \(T_{\text{ON}}\): ON time of PWM signal  
- \(T\): total time period  

### DC motor speed relationship

\[
N \propto V
\]

Where:
- \(N\): motor speed  
- \(V\): applied armature voltage  

## Experimental results

- Achieved **smooth and efficient speed regulation** across a wide operating range.
- Arduino PWM effectively controlled speed **without significant power loss**.
- Direction control worked reliably via H-Bridge configuration.
- LCD provided accurate real-time monitoring of speed (%) and direction.

## Conclusion

This project demonstrates an efficient and precise PWM-based DC motor speed control solution using Arduino and an L298N driver. It highlights the benefits of PWM—**higher efficiency, reduced power loss, and improved speed stability**—and provides practical exposure to embedded systems, power electronics, and motor drives used in automation, robotics, EVs, and mechatronics.

## References

1. Muhammad H. Rashid, *Power Electronics: Circuits, Devices and Applications*, Pearson Education, 4th Edition.
2. L298N Motor Driver Datasheet, STMicroelectronics.
