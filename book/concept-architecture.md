# Architectural Overview

PX4 consists of two main layers: The [PX4 flight stack](concept-flight-stack.md), an autopilot software solution and the [PX4 middleware](concept-middleware.md), a general robotics middleware which can support any type of autonomous robot.

All [airframes](airframes-architecture.md), and in fact all robotic systems including boats, share a single codebase. The complete system design is [reactive](http://www.reactivemanifesto.org), which means that:

  * All functionality is divided into exchangable components
  * Communication is done by asynchronous message passing 
  * The system can deal with varying workload

In addition to these runtime considerations, its modularity maximizes [reusability](https://en.wikipedia.org/wiki/Reusability).
