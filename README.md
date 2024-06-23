# klipper-config-prusa-mk1maaajaaaUpgrade
Klipper config files for my custom upgrade Prusa MK1 with LCD interface similar to the Prusa Original Firmware

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
  
Optional Features (added 09/09/2022):

to be enabled by uncommenting (deleting the #) in the file printer.cfg 

#[include config/custom/menu_autoload.cfg] --> creates autoload/unload filament entries in the Preheat menu (macro to automatically heat to a certain temperature, load/unload the filament, then cooldown)

#[include config/custom/macro_cold_pull.cfg] --> creates automatical Coldpull entry in the Preheat Menu (preheat to selectable temperature [default 85°C for PLA], then automatically coldpull using the motor, no hand pull required, it works very well for PLA at 85 °C, beep at the end to alert the user [remember to pull the lever on the extruder to extract the filament after the automatic coldpull])

#[include config/custom/filament_diameter.cfg] --> enable the "correct filament diameter" feature in the Tune menu, to change the filament diameter during printing, use the 

	M404 W{filament_diameter[0]}; 
	
command in the start GCODE to let Klipper know the filament diameter initially used in the slicer, then you can change the filament diameter on the flight while printing (for example if you use a different spool of filament)

#[include config/custom/accelerometer.cfg] --> config for Raspberry Pi with adxl345 accelerometer for resonance testing (input shaper calibration)
