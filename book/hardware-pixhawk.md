# Pixhawk Hardware

[Pixhawk](https://pixhawk.org/modules/pixhawk) is the standard microcontroller platform for the PX4 flight stack. It runs the PX4 Middleware on the [NuttX](http://nuttx.org) OS. As a CC-BY-SA 3.0 licensed Open Hardware design, all schematics and design files are [available](https://github.com/PX4/Hardware). The [Pixfalcon](hardware-pixfalcon.md) is a smaller version of Pixhawk for FPV racers and similar platforms. For drones requiring high processing performance or a camera interface the [Snapdragon Flight](hardware-snapdragon.md) might be a more optimal fit.

![](images/hardware/hardware-pixhawk.png)

## Quick Summary

  * System-on-Chip: [STM32F437](http://www.st.com/web/en/catalog/mmc/FM141/SC1169/SS1577/LN1789)
    * CPU: 180 MHz ARM Cortex M4 with single-precision FPU
    * RAM: 256 KB SRAM (L1)
  * Wifi: ESP8266 external
  * GPS: U-Blox 7 / M8
  * Video: -
  * Flow: PX4 Flow unit
  * Availability: [3D Robotics Store](https://store.3drobotics.com/products/3dr-pixhawk)

## Connectivity

  * 1x I2C
  * 1x CAN (2x optional)
  * 1x ADC
  * 4x UART (2x with flow control)
  * 1x Console
  * 8x PWM with manual override
  * 6x PWM / GPIO / PWM input
  * S.BUS / PPM / Spektrum input
  * S.BUS output

## Pinouts and Schematics

The board is documented in detailed on the [Pixhawk project](https://pixhawk.org/modules/pixhawk) website.
