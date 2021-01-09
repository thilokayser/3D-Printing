# Printer: Artillery Sidewinder X1

### Start Code 

```
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
```


### End Code

```
G91; relative positioning
G1 Z1.0 F3000 ; move z up little to prevent scratching of print
G90; absolute positioning
G1 X0 Y200 F1000 ; prepare for part removal
M104 S0; turn off extruder
M140 S0 ; turn off bed
G1 X0 Y300 F1000 ; prepare for part removal
M84 ; disable motors
M106 S0 ; turn off fan
```

### Calibrated E Steps 

#### ALT 20.12.20

```
M92 E445.7429048414024 ;Calibrated E Steps 
````

#### Aktuell 02.01.20

```
M92 E445.74 
=
M92 X80.12 Y80.12 Z399.78 E445.74
```

#### Neu 02.01.20
```
M92 E498.3428571428571 
```


# PID Tuning

#### Auto PID Extruder; mit 200 °C; 8 Zyklen
```
M106 S255; Fan 100%
M303 E0 S200 C8
```

#### Auto PID BED; mit 60 °C; 8 Zyklen

```
M303 E-1 S60 C8
```


### Extruder Alt Stock Einstellungen 09.01.20

```
  M301 P14.58 I1.14 D46.57
  M304 P244.21 I45.87 D325.08
```

### Extruder New
```
DEFAULT_Kp 33.18
DEFAULT_Ki 4.82
DEFAULT_Kd 57.08
```

## Extruder New Results apply
```
M301 P33.18 I4.82 D57.08
```

## Bed old Settings
```
M304 P244.21 I45.87 D325.08
```
## Bed new Settings
```
DEFAULT_bedKp 104.05
DEFAULT_bedKi 20.16
DEFAULT_bedKd 134.25
```
## Extruder New Results apply
```
M304 P104.05 I20.16 D134.25
```


