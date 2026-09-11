# 3D CAD

This directory contains all the 2D/3D models for components which are 3D printed or made from sheet metal.

![Image showing the 3D components in this directory against a 1cm grid.](./light-and-switch-parts.jpg) 

```
.
├── 5mm-light-cover-decorator-ring.FCStd       # Black ring around the LED diffuser
├── 5mm-light-cover-decorator-ring-Fillet.step 
├── 5mm-light-cover.FCStd                      # LED diffuser
├── 5mm-light-cover-Revolve.step
├── Front-Panel-Assy.FCStd                     # Minimal assembly to check part alignment
├── Front-Panel.FCStd                          # User-facing front panel
├── Front-Panel-Unfold.dxf                     # FP. Order 0.1" sheet metal
├── Front-Panel-Rear-Plate.FCStd               # Mounting plate for switches and FP PCB
├── Front-Panel-Rear-Plate-Unfold.dxf          # FP PCB plate. 0.1" 5052 Al, K=0.4, R=0.125", 90 degree bend
├── Outlet-Panel.FCStd                         # Panel for Relay Board and Outlets.
├── Outlet-Panel-Assy.FCStd                    # Minimal assembly to check component alignment
├── Outlet-Panel-Unfold.dxf                    # Panel for Relay Board and Outlets. 0.1" 5052 Al, K-0.4 R=0.125", 90 degree bend, M3 hardware
├── Paddle-Switch-Bracket-Cut2.step            # Mount/pivot bracket for paddle switch
├── Paddle-Switch-Bracket-Cut.step             # Mount/pivot, slightly wider for 3D printing
├── Paddle-Switch-Bracket.FCStd
├── Paddle-Switch-Bracket-Unfold.dxf           # Mount/pivot. mild steel 0.03" thick K=0.36, 90 degree bends
├── Paddle-Switch-Bracket-inner-die.FCStd
├── Paddle-Switch-Bracket-inner-die-v1.0A0.step # "Die" for forming the Paddle-Switch-Bracket
├── Paddle-Switch-Cut.step                     # Paddle switch handle, "square"
├── Paddle-Switch.FCStd
├── Paddle-Switch-Fillet.step                  # Paddle switch handle, "rounded"
├── Relay-PCB-Insulator.FCStd                  # Electrical insulator for under the relay board
├── Relay-PCB-Insulator-Unfold.dxf             # 0.03" polypropylene
├── serial-relay-panel.FCStd                   # Reference (potentially out of date) 3D model of the relay PCB
├── serial-relay-panel.step
├── serial-switch-panel.FCStd                  # Reference (potentially out of date) 3D model of the input PCB
└── serial-switch-panel.step
```

Everything has been designed in FreeCAD, but this directory also contains the STEP file from the latest "working" version of the file so you shouldn't need to edit the FCStd files unless you want to tweak them.

## Print Settings

I have printed my copies in PETG (Prusa and Creality) and the following settings work well with a 0.4mm nozzle.

**light cover decorator ring**

* Color: black
* 0.1mm layer height.

**light cover**

* Color: translucent
* 0.1mm layer height
* Print facing upwards so it looks like a small mushroom. Use supports under the outer brim. No supports needed on the inside.
* 100% infill, concentric

**paddle switch bracket**

* Color: any ("Chalky blue" pictured above)
* 0.1mm layer height
* Add support material within the pivot holes on either side. You may need a 3/32" bit to clean the hole afterwards.
* Wait for the bed to cool completely before removing!
* Note: there is also a `.dxf` file if you want this made from sheet metal. See the dir listing comments for details.

**paddle switch bracket die**

* Color: any
* 0.15mm or smaller layer height
* 100% infil
* I used PETG, but I imagine other materials would work fine.
* This is not a piece used in the final assembly, but rather a tool to enable bending of the paddle switch bracket, should you decide to have it made from sheet metal. To do this, print the die and screw down the bracket to the die at one end plus the center hole. Make sure all holes are aligned. Now use a hammer and bend the tabs down until they are nearly flush with the sides of the die. I was able to get fairly consistent results at about 2-3 minute cycle time per switch bracket but YMMV. (Alternatively, just have the sheet metal fab house bend these).

**paddle switch**

* Color: any ("Chalky blue" pictured above)
* 0.1mm layer height
* Print on its side like the above image
* Use supports for all overhangs (around the pivot and the inside ledge)

## Non-printed items

To assemble the outlet panel, you'll need the following components:

* `LSP10120S` from Littelfuse (surge supressor, wire in parallel mode)
* `FL1M-6CW-4-R110V` or any other line voltage panel-mount indicator
* `3-2486200-9` from TE Connectivity or similar panel mount circuit breaker
* `15SRB8-W` from TE Connectivity or similar 15A IEC inlet plug

My recommended power cord is the `P007-006-15D` as it's rated for 15A and has a nice 90-degree plug for fitting behind the workbench.

