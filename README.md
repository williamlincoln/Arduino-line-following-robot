
# White Line-Following Robot (Arduino UNO R4)

An autonomous robotics project featuring an **Arduino UNO R4** designed to navigate a track by detecting a white line on a black surface using infrared logic.

## 📝 Project Description
This robot uses two IR reflection sensors to track a white path. Unlike traditional black-line followers, this build uses "inverted logic" to stay on course. The high clock speed of the **R4 Minima/WiFi** ensures rapid sensor polling, resulting in smoother transitions and better performance on sharp curves.

---

## 🛠️ Hardware Parts List

### **Core Components**
* **Microcontroller:** Elegoo UNO R4 (Minima or WiFi)
* **Chassis:** 2WD (Two-Wheel Drive) Smart Robot Car Chassis Kit
* **Sensors:** 2x Elegoo IR Reflection Sensors (Line Trackers)
* **Motor Driver:** L298N Dual H-Bridge Module

### **Power & Connectivity**
* **Logic Power:** 9V Battery (powers the Arduino R4)
* **Motor Power:** 4x AA Batteries (6V total for DC motors)
* **Wiring:** Male-to-Female & Male-to-Male Jumper Wires
* **Track:** Matte black surface with White Electrical Tape

---

## 🔌 Pin Mapping

| Component | Arduino Pin |
| :--- | :--- |
| **Left IR Sensor** | Pin 2 |
| **Right IR Sensor** | Pin 3 |
| **Left Motor (IN1, IN2)** | Pins 5, 6 |
| **Right Motor (IN3, IN4)** | Pins 9, 10 |


---

## ⚙️ How It Works (White Line Logic)
The IR sensors emit infrared light and measure the reflection. 
1. **On Black Surface:** Low reflection is detected. The motors drive straight.
2. **On White Line:** High reflection is detected.
   * If the **Left Sensor** hits white, the robot pivots **Left**.
   * If the **Right Sensor** hits white, the robot pivots **Right**.
3. **Dual Power:** By separating the Arduino power (9V) from the Motor power (AA batteries), we prevent electrical noise from the motors causing the Arduino to reset.

---

## 🚀 Improvements made to this version
* **R4 Integration:** Optimized for the 5V logic of the UNO R4.
* **Refined Logic:** Adjusted sensor thresholds for high-contrast white-on-black detection.
* **Wire Management:** Grouped pin assignments to avoid Timer conflicts with the Servo library.

---

## ❓ Questions or Feedback?
Feel free to comment on the commit history or open an issue if you have questions abot this project

---

## Parts links
https://www.amazon.com/ELEGOO-Board-ATmega328P-ATMEGA16U2-Compliant/dp/B01EWOE0UU/ref=sr_1_23?crid=3E20SBR2YSH5N&dib=eyJ2IjoiMSJ9.WqU-Fj-ghzrQEQi_6K5QtYNmHk6FW8tr7Xm95PmTbxxdNjpADdG4mJXtA-0V4LMq8ssUMdQqP5V8vUN231YhlYBYIkBmZ1uOp-HaUHA7x99C0i2AP4xaBm6EO0psqnQwLfvMjoGJ4gZV96fRob0xjGg3Gt6Q9HV_30bY9l2vzQyVmW8qCCG20jkq2SI8expR7DwbicPy-BqzAiGoOHEEF-KDk7aiYG0F1fkfKWAP05o.lKbSxSKyr3_n6juYekAj0kGLqZrNut_UFJCaqdcjkjI&dib_tag=se&keywords=arduino+line+following+car&qid=1773171324&sprefix=arduino+line+following+car%2Caps%2C154&sr=8-23
