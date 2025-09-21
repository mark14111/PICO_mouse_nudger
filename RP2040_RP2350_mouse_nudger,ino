/*
 * Created by Mark Lewis
 *
 * This code is in the public domain
 *
 * Tutorial page: Figure it out for yourselves
 *
 * This code nudges your mouse pointer alternately one pixel to the right and one pixel to the left 
 * every 4 minutes (adjust time to suit your screen lock timer).
 *
 * Tested on RP2040 and RP2350 boards
 */

#include "Mouse.h"

unsigned long nudgeMillis = 0;
const unsigned long maxTimeBetweenNudges = 240000; // 4 minutes
bool left = false;

void setup() {
  Serial.begin(9600);  // make it look like a com port
  Mouse.end();
}

void timeToNudge (){
  //check millis since last nudge
  unsigned long currentMillis = millis();
  if ((currentMillis - nudgeMillis) > maxTimeBetweenNudges) {
    Mouse.begin();
    if (left == true) {
      Mouse.move(-1, 0);  
      left = false;
    } else {
      Mouse.move(1, 0);
      left = true;  
    }
    Mouse.end();
    nudgeMillis = millis();
  }
}

void loop() {
  timeToNudge ();
}
