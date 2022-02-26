# klipper-config-prusa-mk2s
Klipper config files for Prusa MK2s with LCD interface similar to the Prusa Original Firmware

Please notice that you could need to adjust the probe offsets slightly in config/mk2s/probe.cfg since the values from the Original Prusa Firmware were not well centered in my setup

Pressure advance values I found on my system (to be used in Filament-->Custom GCode--> Start GCODE):

0.4mm Nozzle:

  ASA (including Z_OFFSET for the PINDA PROBE respect to PLA): 
	
    SET_GCODE_OFFSET Z_ADJUST=-0.09 MOVE=1
    SET_PRESSURE_ADVANCE ADVANCE=0.078
    
  ABS (including Z_OFFSET for the PINDA PROBE respect to PLA): 
	
    SET_GCODE_OFFSET Z_ADJUST=-0.09 MOVE=1
    SET_PRESSURE_ADVANCE ADVANCE=0.105
    
  PETG (including Z_OFFSET for the PINDA PROBE respect to PLA):
	
    SET_GCODE_OFFSET Z_ADJUST=-0.09 MOVE=1
    SET_PRESSURE_ADVANCE ADVANCE=0.1
  
  PLA: 
	
		SET_PRESSURE_ADVANCE ADVANCE=0.0775
  
