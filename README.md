# esp32-watering
Project log for an ESP32 controlled watering system.

## Requirements
- Must be able to stand alone of Home Assistant. If HA goes offline for whatever reason, no plants should die! 
- Fault tolerant. Strive for professional, accept that I am merely a maker. 
- Ability to control water 'dosage' -- good plant parents know that watering shouldn't neccesarily be done on a schedule, and not all plants require watering consistently.
- Moisture sensors are out of scope. There are plenty of commercial solutions out there already.
- Ability to detect when the storage tank runs dry and notify me.
- Packaged up in a neat, small profile package. No jiffy or (obviously) 3D printed jank. 
- Runs off USB-C. Probably 12V at this stage given the pumps and solenoids I'm seeing. 
- If possible, control from the ESP-32 D1 Mini form factor. I use a number of these prototyping boards already.
- Because I now have the "can design PCB" badge, assume order of 5 boards. Let's centralise as much as we can, but make the process reasonably repeatable if I want to run 2/3 zones down the track. 

## To Do
- Peristaltic pump to transfer the water from the tank to the plants
- Micro solenoids (NC) to control the flow to individual drippers (bonus points for daisy chained ones)
- Dripper heads + tube (preferably black)
- Float switch for water (simple circuit, only requires pull-down resistor)
- Container to store water
- Figure out pump flow rate -- we'll use this to set a default run time in ESPHome.
- Relays to control solenoid + pump. Could go with a H-bridge, but don't think we need PWM.
- Industrial design for box -- have seen cylindrical units.
- Most solenoids seem to run on 12V -- have plenty of sealed buck converters sitting around. Will break this out and have a 12V in and 5V in JST on the PCB.

More to follow! 