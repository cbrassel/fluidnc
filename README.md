# fluidnc

Here's my own fluidnc configuration for a 1500x1500 bulkmann3D CNC with an X-Pro V5 controller.

The spindles VFD is a H100 type controler using the RS485 serial connection. As of today I had no communication problem with the VFD, I have used no resistor nor optic isolation, a simple short twisted pair cable. The only drawback is to pay attention on the starting sequence: 
1. X-Pro controler and VFD are switched on at the same time.
2. The PC or at least the serial connection to the PC should come after controler and VFD start

If you want to use this config, please pay attention to the Y-axis homing configuration. 
In my case, the Y-axis end switches (yes they are one on each Y axis) are mounted on the front of the CNC to allow visual control of the switches and easy cleaning of them.

So if the absolute positions are negative on the X and Z axes, they'll be positive on the Y axis. This in no way hinders g-code execution, but you do need to be careful when using G53 G0 Y... type commands.

The openbuilds Fusion Processor is a slightly modified version including the default Y change, I have also added the use of the M7 command that turns the vacuum on when selecting the vaccum in the tool selection of Fusion.

Any comments are welcome.
