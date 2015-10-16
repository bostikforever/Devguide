# UAVCAN Firmware Upgrading

## Vectorcontrol ESCs

Download and build the ESC code:

<div class="host-code"></div>

```sh
git clone https://github.com/thiemar/vectorcontrol
cd vectorcontrol
BOARD=px4esc_1_6 make && BOARD=s2740vc_1_0 make
```

This will build the UAVCAN node firmware for both suppoerted ESCs. The UAVCAN node file naming
follows a strict naming scheme to allow an autopilot to upgrade all devices on the network.

  ```<node name>-<hw version major>.<hw version minor>-<git commit hash>.uavcan.bin```

However, due to space/path length/performance constraints, the UAVCAN firmware updater requires those filenames to be split and stored in a directory structure like the following:

  ```/fs/microsd/fw/<node name>/<hw version major>.<hw version minor>/<git commit hash>.bin```

The ROMFS-based updater follows that pattern, so you add the firmware in:

  ```/etc/uavcan/fw/<node name>/<hw version major>.<hw version minor>/<git commit hash>.bin```

The git commit hash is not validated so it can actually be anything.

## Placing the binaries in the PX4 ROMFS

The resulting finale file locations are:

  * SV2740 ESC: ```ROMFS/px4fmu_common/uavcan/fw/com.thiemar.s2740vc/v1.1.0/00000000.uavcan.bin```
  * Pixhawk ESC: ```ROMFS/px4fmu_common/uavcan/fw/org.pixhawk.px4esc/v1.1.0/00000000.uavcan.bin```

Note that the ROMFS/px4fmu_common directory will be mounted to /etc on Pixhawk.
