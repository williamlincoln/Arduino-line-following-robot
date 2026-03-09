

-----------------------------------------------------------------DESCRIPTON-----------------------------------------------------
  This is a arduino line following robot that follows a white line.
-----------------------------------------------------------------PARTS----------------------------------------------------------
  It uses 2 elgoo color sensors a elgoo uno r4 board 2WD (Two-Wheel Drive) 
Smart Robot Car Chassis Kit. Male to femail whires a 9 volt battery (to power the arduino r4) 4 doble a batterys and eletrical tape 
-----------------------------------------------------------------HOW TO BUILD----------------------------------------------------
It takes about 20-30 minutes to build. use the instructons in the kit to build the frame, moters, batery pack, and power converter 
(the frame, moters, batery pack, and power converter are all in the kit)
----------------------------------------------------------------PINS--------------------------------------------------------------
Component            Arduino pin
Left Motor (IN1)      Pin 5
Left Motor (IN2)      Pin 6
Right Motor (IN3)     Pin 9
Right Motor (IN4)     Pin 10
Left IR Sensor        Pin 2
Right IR Sensor       Pin 3
(The motor whiers have to be pluged into the Power converter first)
-------------------------------------------------------------Finishing Touches----------------------------------------------------
Download this code into the robot to make it work (make sure the green light on each color sensor turns on on white and off on black if not adjust the 
gray screw in the blue box) Ensure both IR sensors are at equal height and distance from the line
Misalignment causes the robot to veer
-----------------------------------------------------------CODE------------------------------------------------------------------------
#include <Servo.h>

// PIN DEFINITIONS
int leftSensor = 2; 
int rightSensor = 3;
int IN1 = 5, IN2 = 6, IN3 = 9, IN4 = 10; 

Servo servo1;
Servo servo2;

void setup() {
  pinMode(leftSensor, INPUT);
  pinMode(rightSensor, INPUT);
  pinMode(IN1, OUTPUT); pinMode(IN2, OUTPUT);
  pinMode(IN3, OUTPUT); pinMode(IN4, OUTPUT);

}

void loop() {
  int L = digitalRead(leftSensor);
  int R = digitalRead(rightSensor);

  // Simple High-Power Logic (No PWM to avoid vibration)
  if (L == LOW && R == LOW) {
    // Forward
    digitalWrite(IN1, HIGH); digitalWrite(IN2, LOW); 
    digitalWrite(IN3, HIGH); digitalWrite(IN4, LOW); 
  } 
  else if (L == HIGH && R == LOW) {
    // Left Turn
    digitalWrite(IN1, LOW);  digitalWrite(IN2, LOW); 
    digitalWrite(IN3, HIGH); digitalWrite(IN4, LOW); 
  } 
  else if (L == LOW && R == HIGH) {
    // Right Turn
    digitalWrite(IN1, HIGH); digitalWrite(IN2, LOW); 
    digitalWrite(IN3, LOW);  digitalWrite(IN4, LOW); 
  } 
  else {
    // Stop
    digitalWrite(IN1, LOW); digitalWrite(IN2, LOW); 
    digitalWrite(IN3, LOW); digitalWrite(IN4, LOW); 
  }
}
