# **L293D Motor Driver IC**

![](https://components101.com/sites/default/files/inline-images/L293D-circuit.png)
## **Overview**
The **L293D** is a popular motor driver IC used to control the speed and direction of DC motors and stepper motors. It acts as a bridge between low-power microcontroller signals and high-power motors, amplifying the signal to drive the motors effectively.

---

## **Features**
- **Dual H-Bridge:** Can control two DC motors independently or one stepper motor.
- **Voltage Range:** Operates between 4.5V and 36V.
- **Current Capacity:** Provides up to 600mA per channel (1.2A peak).
- **TTL Compatible:** Accepts low-power control signals from microcontrollers like Arduino or Raspberry Pi.
- **Built-in Diodes:** Protects against back EMF generated by motors.

---

## **Key Components and Functions**

### **H-Bridge**
- The L293D contains **two H-bridge circuits**.
- An H-bridge allows current to flow in either direction through the motor, enabling forward and reverse motion.
- By activating specific transistors in the H-bridge, the motor direction is controlled.

| Input Pins | Motor Direction |
|------------|-----------------|
| IN1 = HIGH, IN2 = LOW | Forward        |
| IN1 = LOW, IN2 = HIGH | Reverse        |
| IN1 = IN2 (HIGH or LOW) | Stop (Brake) |

### **PWM (Pulse Width Modulation)**
- PWM is used to control motor speed by varying the duty cycle of the signal sent to the input pins.
- A higher duty cycle increases motor speed, while a lower duty cycle slows it down.
- PWM can be generated using microcontrollers like Arduino and applied to the enable pins (EN1/EN2).

### **Pin Configuration**
- **Input Pins (IN1, IN2, IN3, IN4):** Control the direction of the motors.
- **Output Pins (OUT1, OUT2, OUT3, OUT4):** Connect to the motor terminals.
- **Enable Pins (EN1, EN2):** Activate the corresponding H-bridge. Also used for speed control via PWM.
- **Power Pins (VSS, VS):**
  - VSS: Logic power (5V).
  - VS: Motor power supply (up to 36V).

---

## **How to Use L293D**
1. **Connect Motor Wires:**
   - Attach the motor terminals to the output pins (OUT1/OUT2 or OUT3/OUT4).
2. **Provide Power:**
   - Connect 5V to VSS for logic and appropriate voltage (4.5–36V) to VS for the motors.
3. **Connect Control Pins:**
   - Link IN1/IN2 (or IN3/IN4) to the microcontroller's GPIO pins.
   - Enable the motor channel using EN1/EN2.
4. **Control Speed and Direction:**
   - Change the HIGH/LOW signals at the input pins to reverse motor direction.
   - Use PWM at the enable pins to adjust motor speed.

---

## **Applications**
- **Robotics:** Driving wheels of robots.
- **DIY Projects:** Automated gates, conveyor belts, or robotic arms.
- **Stepper Motor Control:** Precise movement for CNC machines or 3D printers.

---

## **Advantages**
- Simple and easy to use.
- Can control two motors simultaneously.
- Provides protection from back EMF.

---

## **Limitations**
- Limited current capacity (600mA per channel).
- Heat dissipation may require a heat sink for extended operation.
- Inefficient compared to modern motor drivers.

---

The **L293D IC** is a versatile and budget-friendly solution for motor control in a wide range of applications, making it an excellent choice for beginners and hobbyists.
