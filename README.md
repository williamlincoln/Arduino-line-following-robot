
# White Line-Following Robot (Arduino UNO R4)

An autonomous robotics project featuring an **Arduino UNO R4** designed to navigate a track by detecting a white line on a black surface using infrared logic.

## 📝 Project Description
This robot uses two IR reflection sensors to track a white path. Unlike traditional black-line followers, this build uses "inverted logic" to stay on course. The high clock speed of the **R4 Minima/WiFi** ensures rapid sensor polling, resulting in smoother transitions and better performance on sharp curves.

---

## 🛠️ Hardware Parts List
It is $57.02 in total for all the things
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
* **Batery holder:** https://www.amazon.com/ZRM-Battery-5-5x2-1-Connector-Arduino/dp/B08P1L6JQT/ref=sr_1_8?crid=UFBHQ90O2O3H&dib=eyJ2IjoiMSJ9.037O6BoEfSUcbYaUoB1nAbyk_2tgZ4LuqhBY2jgbu32fOWWDZV-yoahFO0aKivO5cRzPa46KoLnkPgvsHGzqMwqyxXTwOyRu78bVQSbHlnXC5QSvkuwdCwTuypohTG2lXWkuM-DzdMx4HgnbVhVqAcZ-LvRjfJu7EdN-j0ofsw7ZOFGGiPKZfepty3fPXv6b55Ln0-meSuiQq672_UR8b1gjDRPuUp96zERXMYRtKxn-X7hTWMsxvPVRP0Ks6V0GpibwA1SjxoRFUzX8D4P806afJhCbQqrUSm6ZRxd8GNM.FoDfFgDsnHWfDSrmExBY2OvgrDPIUHaEO8FZqmHyD-s&dib_tag=se&keywords=12v+arduino+battery&qid=1773171995&sprefix=12v+arduino+battery%2Caps%2C215&sr=8-8
* **Electrical wires:** https://www.amazon.com/BNTECHGO-Electric-Gauge-Tinned-Copper/dp/B0852TP6Q5/ref=sr_1_5?crid=K59AG51YK5LZ&dib=eyJ2IjoiMSJ9.IxWTtTLjT3jZUpuRfg4Wd-ZMdYX6be1-GXWuZIEN9Zb2pQjrfdsYmpsHfADi0E5DGz5dR5nYGH6tEx433o58tEgyxcpC5CxEzPst-VRivN33hlPnyObWXjvXDDS3r5lhEKJfmRHDqZoBbBo2JCGXk0a5R5Dgk8hV2_xRvs0MlRJDM7dE3LCd6lkgF0Su3MSFHxmUsGw8tGEvPvcyz2CRElSHPmoVDemFeb6EENyzHAY.WjzNMrnUTtmtweKC__8anxklNyYEn16u-qz4TqlIG0M&dib_tag=se&keywords=arduino%2Bwires&qid=1773172113&sprefix=arduino%2Bwires%2Caps%2C187&sr=8-5&th=1
* **Batterys (you need eight batterys in total):** [https://www.amazon.com/Energizer-Batteries-Pack-Double-Alkaline/dp/B0D51V5K5J/ref=sr_1_17?crid=3MXEEFWT841VA&dib=eyJ2IjoiMSJ9.APMTKktpxODsDRlZ8IR_790zN6QJCAJi3HQaNtsTkhu5iESTU55Xjb0oobtQQ00mZwPiisQI47zSAeHNZSpxMhScOfr8Hpj8SD2Nw8JnGXl2pL9bJw3Z-MwpZCJob0cF-bFs_sETJPCyCddyRB4aiZwNbAN2Z_lD2rIL7h1E-dGwb7hSa57qOyCTHuovBUtIb_VDiPh4TVIeIkRq2SIUBEI97xTwyQWL8lUZ8SnNz_Ur8VAMwI7xRZT01L9pbUlnXgGzAWJ7RXJQ_cDavQ9ix8ssOZU4gef4o32stRTXJBk.QGlEmpJJGXydHkNf2KDduotXT-D-SOinGt5vFGwyTvE&dib_tag=se&keywords=double%2Ba%2Bbatteries&qid=1773172276&sprefix=double%2Caps%2C222&sr=8-17&th=1](https://www.amazon.com/Duracell-CopperTop-Batteries-All-Purpose-Household/dp/B00000JHQ6/ref=sr_1_12?crid=180VQVH7VGDRK&dib=eyJ2IjoiMSJ9.9BhQMbW-D1k7f1etQtjFXpFJrbsz407aoe9KeqjaSYqV8f2eg_TFPpONQzp053NN8hllgCAKvFVvc40kCuNKNxVnPWvyaGg7E2F2tBUdQdL5oYtTjQus2SyQZSxdIChl8eBbTdvPL7iLV11Mzvg7iqvNcZy-fvCtmwvefI-cs-gbjLOIFWlEgD0Zn9Xqx1pyEWX8q8X6-hfyqpHvetSDvj_UhrhyIOw4ir2CA91Wh8iQO39Lmz4y2kWomxu48kjMRSmuIp8wlmNV38qGY7CGqSUKHVad_lIy7Sw_xctta3M.6VbEUPsNj05aff5fMr6jM_2OzwhZVXWDczSIFBQu_bI&dib_tag=se&keywords=double%2Ba%2Bbatteries&qid=1773172738&sprefix=double%2Ba%2Bbatteries%2Caps%2C264&sr=8-12&th=1)
* **Color senser (you need two):** https://www.amazon.com/Mixse-Infrared-IR-Obstacle-Avoidance/dp/B076QGXGRP/ref=sr_1_1?crid=1DI08AG66VKXE&dib=eyJ2IjoiMSJ9.iZD2tYgNPd1GHie6l8emrsdbnlAEXQ62MUK0FineJYuyVf9NbaaGovAbkjrCAX_VwOIy2DY_nn5yWFIzjD5TiYo8rDUYWaBcXW3i6GMeAbG6UmZ8WPaz88ZcUX72ruVLjwaBouA4a93L6lAvpT17G-wGq1S_z-FUEKDTerjllwcIInFcha0wwoyHKECSY5v0DWx0EbFMWdIEXlWC6LA2DwpNOOpr0_olS9dylqhjjtw.QK2uVp3VjMcZEUh7_Y3RHWFF66Aw7L3nd3tIHSEjnyQ&dib_tag=se&keywords=arduino+infrared+sensor+2+pack&qid=1773172489&sprefix=arduino+infared+sensor+2+pack%2Caps%2C155&sr=8-1&xpid=7AMDi5j_pLZzb

---

## Code

C++
#include <Servo.h>

// PIN DEFINITIONS

int leftSensor = 2; 

int rightSensor = 3;

int IN1 = 5, IN2 = 6, IN3 = 9, IN4 = 10; 

void setup() {

  pinMode(leftSensor, INPUT);
  pinMode(rightSensor, INPUT);
  pinMode(IN1, OUTPUT); 
  pinMode(IN2, OUTPUT);
  pinMode(IN3, OUTPUT); 
  pinMode(IN4, OUTPUT);
}

void loop() {
  int L = digitalRead(leftSensor);
  int R = digitalRead(rightSensor);

  // LOGIC: White Line Detection (HIGH = White, LOW = Black)
  if (L == LOW && R == LOW) {
    forward(); 
  } 
  else if (L == HIGH && R == LOW) {
    turnLeft(); // Left sensor hit white, adjust left
  } 
  else if (L == LOW && R == HIGH) {
    turnRight(); // Right sensor hit white, adjust right
  } 
  else {
    stopBot(); 
  }
}

void forward() {
  digitalWrite(IN1, HIGH); digitalWrite(IN2, LOW); 
  digitalWrite(IN3, HIGH); digitalWrite(IN4, LOW); 
}

void turnLeft() {
  digitalWrite(IN1, LOW);  digitalWrite(IN2, LOW); 
  digitalWrite(IN3, HIGH); digitalWrite(IN4, LOW); 
}

void turnRight() {
  digitalWrite(IN1, HIGH); digitalWrite(IN2, LOW); 
  digitalWrite(IN3, LOW);  digitalWrite(IN4, LOW); 
}

void stopBot() {
  digitalWrite(IN1, LOW); digitalWrite(IN2, LOW); 
  digitalWrite(IN3, LOW); digitalWrite(IN4, LOW); 
}
