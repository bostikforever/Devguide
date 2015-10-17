# Software in the Loop (SITL) Simulation

Software in the Loop Simulation runs the complete system on the host machine and simulates the autopilot. It connects via local network to the simulator. The setup looks like this:

```mermaid
graph LR;
  Simulator-->MAVLink;
  MAVLink-->SITL;
```

## Running SITL

After ensuring that the [simulation prerequisites](simulation-prerequisites.md) are installed on the system, just launch: The convenience make target will compile the POSIX host build and run the simulation.

<div class="host-code"></div>

```sh
make run_sitl_quad
```
