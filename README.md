# Cashback-bin
//The project is about reduce non-bio-degradable waste. So this project gives cash back on returning waste bottles.
#include <Servo.h>

const int laserPin = 2;
const int servoPin = 9;

Servo myservo;

void setup() {
  myservo.attach(servoPin);
  pinMode(laserPin, INPUT);
}

void loop() {
  int laserState = digitalRead(laserPin);
  if (laserState == HIGH) {
    myservo.write(90);
    myservo.write(0);
    delay(1000);
  } else {
    myservo.write(90);
  }
//this code is for servo motor working
