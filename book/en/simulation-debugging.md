# Simulation Debugging

As the simulation is running on the host machine, all the desktop development tools are available.

## GCC Toolchain (Linux)

## CLANG Toolchain (Mac OS, Linux)

### Address Sanitizer

<div class="host-code"></div>

```clang
-O1 -g -fsanitize=address -fno-omit-frame-pointer
```
