# Stealthburner Heatsink Thermistor Mod for Dragon Hotends
 ### Allows you to monitor the temperature of your heatsink where it mounts to the toolhead. Klipper can be configured to shutdown if this gets too hot in the event of a hotend fan failure.   

<img src="./Images/thermistor.jpeg" width=600>

### BOM
100K Ohm NTC 3950

### Printing
  * Default voron settings
  * No supports needed
  * Only rear portion of Stealthburner is needed to inplement this mod

### Instructions:
 Add a small dab of thermal grease to the thermistor before assembly. 
 
After connecting the thermistor to your control board add your thermistor entry to your printer.cfg file. I recommend setting at a lower shutdown temp to test before setting your final max_temp value
 
printer.cfg example: 

[temperature_sensor heatsink_temp]

sensor_type: Generic 3950

sensor_pin:      #port that thermistor is plugged into

min_temp: 0

max_temp: 50     #halt printer if ABS deflection temp is exceeded set to 90 after sucessful shutdown test at 50

