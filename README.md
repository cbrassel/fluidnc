# fluidnc

Here's my own fluidnc configuration for a 1500x1500 bulkmann3D CNC with an X-Pro V5 controller.

If you want to use this file, please pay attention to the Y-axis homing configuration. 
In my case, the Y-axis end switches (yes they are one on each Y axis) are mounted on the front of the CNC to allow visual control of the switches and easy cleaning of them.

So if the absolute positions are negative on the X and Z axes, they'll be positive on the Y axis. This in no way hinders g-code execution, but you do need to be careful when using G53 G0 Y... type commands.

Any comments are welcome.
