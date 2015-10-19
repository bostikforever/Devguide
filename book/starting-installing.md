# Installing Files and Code

The PX4 code can be developed on [Mac OS](starting-installation-mac.md), [Linux](starting-installation-linux.md) or [Windows](starting-installation-windows.md). Mac OS and Linux are recommended since image processing and advanced navigation cannot be easily developed on Windows. If unsure, new developers should default to Linux and the current [Ubuntu LTS edition](https://wiki.ubuntu.com/LTS).

## Setting up the Development Environment

  * [Mac OS](starting-installation-mac.md)
  * [Linux](starting-installation-linux.md)
  * [Windows](starting-installation-windows.md)

## Compiling on the Console

Before moving on to a graphical editor or IDE, it is important to validate the system setup. Do so by bringing up the terminal. On OS X, hit ⌘-space and search for 'terminal'. On Ubuntu, click the launch bar and search for 'terminal'. On Windows, find the PX4 folder in the start menu and click on 'PX4 Console'.

![](images/toolchain/terminal.png)

The terminal starts in the home directory. We default to '~/src/Firmware' and clone the upstream repository. Experienced developers might clone [their fork](https://help.github.com/articles/fork-a-repo/) instead.

```sh
mkdir -p ~/src
cd ~/src
git clone https://github.com/PX4/Firmware.git
```
Now its time to build the binaries by compiling the source code.

```sh
cd Firmware
make px4fmu-v2_default
```

Note the syntax: 'make' is the build tool, 'px4fmu-v2' is the hardware / autopilot version and 'default' is the default configuration. All PX4 build targets follow this logic. A successful run will end with this output:

```sh
[100%] Linking CXX executable firmware_nuttx
[100%] Built target firmware_nuttx
Scanning dependencies of target build_firmware_px4fmu-v2
[100%] Generating nuttx-px4fmu-v2-default.px4
[100%] Built target build_firmware_px4fmu-v2
```

By appending 'upload' to these commands the compiled binary will be uploaded via USB to the autopilot hardware:

```sh
make px4fmu-v2_default upload
```

A successful run will end with this output:

```sh
Erase  : [====================] 100.0%
Program: [====================] 100.0%
Verify : [====================] 100.0%
Rebooting.

[100%] Built target upload
```

But before going straight to the hardware, a [simulation run](simulation-sitl.md) is recommended as the next step. Users preferring to work in a graphical development environment should continue with the next section.

## Compiling in a graphical IDE

The PX4 system supports Qt Creator, Eclipse and Sublime Text. Qt Creator is the most user-friendly variant and hence the only officially supported IDE. Unless an expert in Eclipse or Sublime, their use is discouraged. Hardcore users can find an [Eclipse project](https://github.com/PX4/Firmware/blob/master/.project) and a [Sublime project](https://github.com/PX4/Firmware/blob/master/Firmware.sublime-project) in the source tree.

Before starting Qt Creator, the [project file](https://cmake.org/Wiki/CMake_Generator_Specific_Information#Code::Blocks_Generator) needs to be created:

```sh
cd ~/src/Firmware
mkdir build_creator
cd build_creator
cmake .. -G "CodeBlocks - Unix Makefiles"
```

That's it! Start Qt Creator, then click on *File -> Open File or Project..* and select the file '~/src/Firmware/build_creator/px4.cbp'. Building (the hammer symbol) now already works, and the correct setup to run the project is explained in the video below.
