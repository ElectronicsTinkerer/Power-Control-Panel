# Custom Remote-Controlled Power Distribution Panel

![Front image of the control panel, showing eight blue switches, grouped by fours, and a single red switch labeled "master" on the right side. Each group is separated by square U-bolts, acting as guards or handles to the panel. Below the switches are large orange indicator bulbs.](images/control-panel-front-installed.JPG)

The control panel provides control over eight individually switched outlets for managing the numerous gizmoes plugged in to your workbench. In addition, there is a master switch which overrides the rest of the panel for shutting down all outputs.

The device is constructed of two components. The first (pictured above) is the control panel. This contains a PCB that uses a shift register to parallel load the state of the input switches and send them over an ethernet-style cable to the second component, the relay board. The relay board is responsible for generating the clock and load signals used by the control panel. It also shifts in the data from the control panel and drives a bank of eight relays to control attached devices.

All the design files are included in this repo. For more background and pictures, checkout [my website](https://zrcn.org/power-control-panel.html).

![Relay board connected to outlets on the top side and protection circuitry on the right.](images/outlet-panel-back.JPG)
![Front of the outlet panel, showing eight outlets, one IEC power inlet plug, the thermal breaker, and the surge supressor status light](images/outlet-panel-front.JPG)
