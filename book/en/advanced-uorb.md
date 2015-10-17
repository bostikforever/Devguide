# uORB Messaging

## Introduction

The uORB is a publish() / subcribe() messaging tool.


## Listing Topics and Listening in

To list all topics, list the file handles:

```sh
ls /obj
```

To listen to the content of one topic for 5 messages, run the listener:

```sh
listener sensor_accel 5
```

The output is n-times the content of the topic:

```sh
TOPIC: sensor_accel #3
timestamp: 84978861
integral_dt: 4044
error_count: 0
x: -1
y: 2
z: 100
x_integral: -0
y_integral: 0
z_integral: 0
temperature: 46
range_m_s2: 78
scaling: 0

TOPIC: sensor_accel #4
timestamp: 85010833
integral_dt: 3980
error_count: 0
x: -1
y: 2
z: 100
x_integral: -0
y_integral: 0
z_integral: 0
temperature: 46
range_m_s2: 78
scaling: 0
```
