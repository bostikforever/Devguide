# Software in the Loop (SITL) Simulation

Software in the Loop Simulation runs the complete system on the host machine and simulates the autopilot. It connects via local network to the simulator.

## Installation

Clone the jMAVSim 

<div class="host-code"></div>

The convenience make target will compile the POSIX host build and run the simulation.

```sh
make run_sitl_quad
```

## Building and Running SITL

<div class="host-code"></div>

The convenience make target will compile the POSIX host build and run the simulation.

```sh
make run_sitl_quad
```

## Installing Packages

```mermaid
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
```
