<!--
---
type: board
name: "Sense HAT"
manufacturer: Raspberry Pi Foundation
description: Add-on board that includes an 8×8 RGB LED matrix, 5-button joystick as well as IMU and environmental sensors
url: https://www.raspberrypi.org/products/sense-hat/
formfactor: 'HAT'
pincount: 40
eeprom: yes
pin:
  '3':
    mode: i2c
  '5':
    mode: i2c
  '16':
    name: Joystick
    mode: input
  '18':
    name: Joystick
    mode: input
  '19':
    mode: spi
  '21':
    mode: spi
  '22':
    name: Joystick
    mode: input
  '23':
    mode: spi
  '24':
    mode: spi
install:
  'devices':
    - 'i2c'
    - 'spi'
-->
#センス・ハット (Sense HAT)

センス・ハットは、ラズベリーパイの拡張ボードで、8x8マトリクスのフルカラーLED、4方向＋1センターボタンのジョイスティックに加え、以下のセンサーから構成されます：

ジャイロスコープ、加速度計、地磁気計、温度計、気圧計、湿度計

LEDマトリクスを駆動するシフトレジスタは、LED2472Gで、ATtiny88経由、パイのSPIバスに接続されています。4方向＋1センターボタンのSKRHABE010ジョイスティックも同様にSPIバスに接続されています。

センサーは、（ほとんど）I2Cバスで動作します：

慣性計測ユニット（ジャイロスコープ、加速度計、地磁気計）は、LSM9DS1を通じてI2Cアドレス0x1c(0x1e)と0x6a(0x6b)にあり、ATtiny88の割り込みを使います。

環境センサーは、I2Cバス上の気圧／温度センサーLPS25H（0x5c）、湿度／温度センサーHTS221（0x5f）で構成されます。
