# UAVCAN Introduction

![](images/uavcan-logo-transparent.png)

UAVCAN is an onboard network which allows the autopilot to connect to motor controllers. It supports hardware like:

  * Motor controllers
    * Pixhawk ESC
    * SV2740 ESC
  * Airspeed sensors
    * Thiemar airspeed sensor
  * GNSS receivers for GPS and GLONASS
    * Zubax GNSS

  In contrast to hobby-grade devices it uses rugged, differential signalling and supports  upgrades over the bus. All motor controllers provide status feedback and implement field-oriented-control (FOC).

## Upgrading Node Firmware

The PX4 middleware will automatically upgrade firmware on UAVCAN nodes if the matching firmware is supplied. The process and requirements are described on the [UAVCAN Firmware](uavcan-node-firmware.md) page.

## Enumerating and Configuring Motor Controllers

The ID and rotational direction of each motor controller can be assigned after installation in a simple setup routine: [UAVCAN Node Enumeration](uavcan-node-enumeration.md).
