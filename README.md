# PICO_mouse_nudger
A small utility that uses the HID capabilities of the RP2040/RP2350 to keep the screen lock from kicking in. Written for Arduino IDE 

Just add the RP2040/RP2350 board to your Additional Boards Manager URLs in the Arduino/Preferences window. Compile and upload to your board.

Nudges the mouse pointer one pixel to the right followed by one to the left every four minutes. Adjust maxTimeBetweenNudges (in milliseconds)
to suit your needs.

It appears as a COM port so your office PC won't scream at you for plugging in a memory stick. 

Have fun on your extended coffee breaks without big brother watching if your are online.
