# Stealthburner Heatsink Thermistor Mod for Dragon Hotends
 ### Allows you to monitor the temperature of your heatsink where it mounts to the toolhead. Klipper can be configured to shutdown if this gets too hot in the event of a hotend fan failure.   

<img src="./Images/thermistor.jpeg" width=600>

### BOM
100K Ohm NTC 3950 glass bead thermistor. (bead should measure approximately 1.6mm diameter x 3.3mm in length)

Here are the ones I use in my printersfor this mod. 
https://www.amazon.com/gp/product/B098TF372P/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1

### Printing
  * Default voron settings
  * No supports needed
  * Only the included rear portion of Stealthburner toolhead is needed to inplement this mod

### Instructions:
 Add a small dab of thermal grease to the thermistor before assembly. 
 
After connecting the thermistor to your control board add the thermistor entry to your printer.cfg file. I recommend setting at a lower shutdown temp to test before setting your final max_temp value
 
printer.cfg example: 

[temperature_sensor heatsink_temp]

sensor_type: Generic 3950

sensor_pin:      #port that thermistor is plugged into

min_temp: 0

max_temp: 50     #halt printer if ABS deflection temp is exceeded set to 90 after sucessful shutdown test at 50

