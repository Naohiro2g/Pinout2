<!--
---
type: board
name: Drum HAT
manufacturer: Pimoroni
description: An 8 pad finger Drum HAT for your Raspberry Pi
url: https://github.com/pimoroni/drum-hat
github: https://github.com/pimoroni/drum-hat
buy: http://shop.pimoroni.com/products/drum-hat
formfactor: 'HAT'
pincount: 40
eeprom: yes
pin:
  '3':
    mode: i2c
  '5':
    mode: i2c
  '22':
    name: Alert
    mode: input
  '40':
    name: Reset
    mode: output
i2c:
  '0x2c':
    name: Cap Touch
    device: cap1188
    datasheet: http://ww1.microchip.com/downloads/en/DeviceDoc/CAP1188%20.pdf
-->
#Drum HAT

Drum HAT is the companion to Piano HAT. It uses the same cap touch sensor to provide 8 finger-sized drum pads. Use it to play music in Python, control software drum synths on your Pi, take control of hardware drum machines, or just build it into an elaborate drum-controlled project.

Features: 8 touch sensitive buttons and 8 LEDs. Works with Piano HAT (it uses a CAP1188 chip with a non-conflicting i2c address at 0x2c).

To get the HAT set up and ready to go you can use the one-line product installer:

```bash
curl -sS get.pimoroni.com/drumhat | bash
```

And follow the instructions!
