# Printer: Artillery Sidewinder X1


### Start Code 

G28 ; home all axes
M117 Purge extruder
G92 E0 ; reset extruder
M92 E445.7429048414024 ;Calibrated E Steps
G1 Z1.0 F3000 ; move z up little to prevent scratching of surface
G1 X2 Y20 Z0.3 F5000.0 ; move to start-line position
G1 X2 Y200.0 Z0.3 F1500.0 E15 ; draw 1st line
G1 X2 Y200.0 Z0.4 F5000.0 ; move to side a little
G1 X2 Y20 Z0.4 F1500.0 E30 ; draw 2nd line
G92 E0 ; reset extruder
G1 Z1.0 F3000 ; move z up little to prevent scratching of surface
M42 P4 S0 ; LED aus
M42 P5 S0 ; LED aus
M42 P6 S0 ; LED aus

---

### End Code

G91; relative positioning
G1 Z1.0 F3000 ; move z up little to prevent scratching of print
G90; absolute positioning
G1 X0 Y200 F1000 ; prepare for part removal
M104 S0; turn off extruder
M140 S0 ; turn off bed
G1 X0 Y300 F1000 ; prepare for part removal
M84 ; disable motors
M106 S0 ; turn off fan


## Calibrated E Steps 
### ALT 20.12.20
M92 E445.7429048414024 ;Calibrated E Steps 

### Aktuell 02.01.20

M92 E445.74 
=
M92 X80.12 Y80.12 Z399.78 E445.74

### Neu 02.01.20

M92 E498.3428571428571 
