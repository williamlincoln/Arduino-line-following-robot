
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
* **Elegoo board:**  https://www.amazon.com/ELEGOO-Board-ATmega328P-ATMEGA16U2-Compliant/dp/B01EWOE0UU/ref=sr_1_23?crid=3E20SBR2YSH5N&dib=eyJ2IjoiMSJ9.WqU-Fj-ghzrQEQi_6K5QtYNmHk6FW8tr7Xm95PmTbxxdNjpADdG4mJXtA-0V4LMq8ssUMdQqP5V8vUN231YhlYBYIkBmZ1uOp-HaUHA7x99C0i2AP4xaBm6EO0psqnQwLfvMjoGJ4gZV96fRob0xjGg3Gt6Q9HV_30bY9l2vzQyVmW8qCCG20jkq2SI8expR7DwbicPy-BqzAiGoOHEEF-KDk7aiYG0F1fkfKWAP05o.lKbSxSKyr3_n6juYekAj0kGLqZrNut_UFJCaqdcjkjI&dib_tag=se&keywords=arduino+line+following+car&qid=1773171324&sprefix=arduino+line+following+car%2Caps%2C154&sr=8-23
* **Chasi kit:** https://www.amazon.com/Smart-Chassis-Motors-Encoder-Battery/dp/B01LXY7CM3/ref=sr_1_2?crid=2HH5TCH8CIPLI&dib=eyJ2IjoiMSJ9.gvOdf6OgRT6s5iMt2pmavy14rIMPBPKSr17ERJYdjZYCxrRs8nLDP5obAxyXCtFwrg-H4XruV7wPIvd_f-gdZ9as9ZkVie4msm1vmrR9CQVGqik6noFewxorpM2LotL1YBeIX0x89_wVMqy589_uAJOQwZgkQJG20fLcI2i8EehFARTqQKw4bs3VtGEftCDIzFYliDHSBan9fPg1sHC8Dgx5dq0vKgwCM37iuQNW_BVsoCYYAoZxtyT8mEN8iohZ8cErw5aKdhbYc790w7meddMJ1F1YtMkXcufzYaHSuFQ.wojnVBMyFgLhwhndKm0QsTW-rBMnwTdNb9qo26vSEQ0&dib_tag=se&keywords=2WD+Smart+Robot+Car+Chassis+Kit.&qid=1773171629&sprefix=2wd+smart+robot+car+chassis+kit.%2Caps%2C179&sr=8-2
* **Male to female wires:** https://www.amazon.com/Solderless-Multicolored-Electronic-Breadboard-Protoboard/dp/B09FPDNHLL/ref=sr_1_17_sspa?crid=3BRTX76X1Z5HV&dib=eyJ2IjoiMSJ9.wEKU50RNolzpGiuWp366RDKiM3riIOzifXAkyawzKekn_MTcIys9_DbCpj4PopH4oxTsRjKfPxcOwtQSCn0tRT3_795WO5GfIfp-ePdub0CY7nAahFCLUWTD9M834weeGrwpbEjttwFqsfj1dNxEt_79083dduOCqIt_Y9e6lEskoy32FSvxCcQByqcN24QU_38SLkfBFG-2P2-r0Nhg7iRDXHWM1aAjLvipZwLl5KQ.QYLQqQ_X46j_jXKWknuVahmVLXz8zCpdOqSaF3VrAUI&dib_tag=se&keywords=male%2Bto%2Bfemale%2Bwires&qid=1773171865&refinements=p_36%3A-1200%2Cp_n_g-1002988121111%3A23641606011%7C23641609011&rnid=1243644011&sprefix=male%2Bto%2Bfemale%2Bwires%2Caps%2C1211&sr=8-17-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9idGY&th=1
