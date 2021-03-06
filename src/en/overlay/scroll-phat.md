<!--
---
type: board
name: Scroll pHAT
manufacturer: Pimoroni
description: A 11 x 5 LED matrix.
url: https://github.com/pimoroni/scroll-phat
github: https://github.com/pimoroni/scroll-phat
buy: https://shop.pimoroni.com/products/scroll-phat
formfactor: 'pHAT'
pincount: 40
eeprom: no
power: 5v
pin:
  '3':
    mode: i2c
  '5':
    mode: i2c
i2c:
  '0x60':
    name: Matrix LED driver
    device: IS31FL3730
install:
  'devices':
    - 'i2c'
  'apt':
    - 'python-smbus'
    - 'python3-smbus'
  'python':
    - 'scrollphat'
  'python3':
    - 'scrollphat'
  'examples': 'examples/'
-->
#Scroll pHAT

The Scroll pHAT provides a matrix of 55 white LED pixels that is ideal for writing messages, showing graphs, and drawing pictures. Perfect for RPi Zero but works with A+/B+/2 too!

To get the pHAT set up and ready to go you can use the one-line product installer:

```bash
curl -sS get.pimoroni.com/scrollphat | bash
```

Then import it into your Python script and start tinkering:

```bash
import scrollphat
```
