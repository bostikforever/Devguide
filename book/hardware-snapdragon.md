# Snapdragon Flight Autopilot

The Snapdragon Flight platform is a high-end autopilot / onboard computer which runs the PX4 Flight Stack on the DSP on the QuRT real time operating system. In comparison to [Pixhawk](hardware-pixhawk.md) it adds a camera and Wifi and high-end processing power, but also has less IO.

![](images/hardware/hardware-snapdragon.jpg)

## Quick Summary

  * System-on-Chip: [Snapdragon 801](https://www.qualcomm.com/products/snapdragon/processors/801)
    * CPU: Up to 2.5 GHz quad-core Qualcomm® Krait™ 400 CPU
    * DSP: 800 MHz Hexagon DSP (running the flight code)
    * GPU: Qualcomm® Adreno™ 330 GPU
    * RAM: 
  * Wifi: Qualcomm® VIVE™ 1-stream 802.11n/ac with MU-MIMO † Integrated digital core
  * GPS: Sirf Star III
  * Video: 4K / H.264 (AVC)
  * Flow: Global shutter
  * Availability: [Intrinsyc Store](http://shop.intrinsyc.com/products/snapdragon-flight-dev-kit)

## Connectivity

  * 1x I2C
  * x UART (2x with flow control)

## Dimensions

![](images/hardware/hardware-snapdragon-dimensions.png)
