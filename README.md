# Moksha-Krishna
#include <LiquidCrystal_I2C.h>
LiquidCrystal_I2C lcd(0x27, 16, 2);
void setup() {
lcd.init();
lcd.backlight();
pinMode(A0, INPUT);
pinMode(A1, INPUT);
pinMode(A2, INPUT);
pinMode(A3, INPUT);
pinMode(A6, INPUT);
Serial.begin(9600);
}
void loop() {
lcd.clear();
if (analogRead(A0) > 600) {
lcd.setCursor(0, 0);
lcd.print("My name is ");
lcd.setCursor(0, 1);
lcd.print("Riya");
delay(500);
}
lcd.clear();
if (analogRead(A1) > 600) {
lcd.setCursor(0, 0);
lcd.print("I live in");
lcd.setCursor(0, 1);
lcd.print("Kochi");
delay(500);
}
lcd.clear();
if (analogRead(A2) > 600) {
lcd.setCursor(0, 0);
lcd.print("I need ");
lcd.setCursor(0, 1);
lcd.print("Medicine");
delay(500);
}
lcd.clear();
if (analogRead(A3) > 600) {
lcd.setCursor(0, 0);
lcd.print("I want to");
lcd.setCursor(0, 1);
lcd.print("go out");
delay(500);
}
lcd.clear();
if (analogRead(A6) > 600) {
lcd.setCursor(0, 0);
lcd.print("I want");
lcd.setCursor(0, 1);
lcd.print("food");
delay(500);}}
