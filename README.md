# Adafruit_FreeTouch [![Build Status](https://github.com/adafruit/Adafruit_FreeTouch/workflows/Arduino%20Library%20CI/badge.svg)](https://github.com/adafruit/Adafruit_FreeTouch/actions)

A QTouch-compatible library for SAMD11 or SAMD21.

## Minimal example

Here's code to enable QTouch on pin PA15 and read measurements in the loop():

```
#include "Adafruit_FreeTouch.h"

[...]

Adafruit_FreeTouch qt(15, OVERSAMPLE_4, RESISTOR_50K, FREQ_MODE_NONE);

void setup() {
  qt.begin();

  [...]
}


void loop() {
  int qt_value = qt.measure(); // read 10-bit value
  
  [...]
}
```
