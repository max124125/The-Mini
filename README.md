
<p float="left">
  <img src="https://github.com/user-attachments/assets/053dbf47-2d4c-473e-b85b-c99c70d783e3" width="350" />
  <img src="https://github.com/user-attachments/assets/052ca413-d359-4bd2-86f1-8dcd0c32871f" width="347"/>

</p>

# The-Mini
The smallest - yet still fully functional - 3D printer I could design.    

Design goals:  
-Other smaller printers of this size used ROM drive steppers. I have oppted to exclude these for the x and y axes as they have very limited accuracy (20steps/mm) compared to traditional Nema 17 based printers (80steps/mm).  
-An additional goal is for this printer to be able to achieve the same speed/accel of a default ender 3 (500mm/s2 at 50mm/s).  
-The entire printer (excluding filament and power supply) needs to fit into the 3x4x5 inch Vaultz lockbox I have (see image).

MAJOR update: The release of the new Micro4 fly board by Mellow has led to a full rebuild of the printer. This is due to the major space savings from the new board. With the older SKR board, the printer was very close to not fitting in the vaultz box (actually tearing some of the fabric, and being hard to close due to the tight fit). But with the new board the printer could easily be up to 5mm shorter, and 10mm thinner. This will hopefully give a lot more comfortable fit and potentially even allow the addition of a small power supply or filament roll to fit in the box with the printer. 

Old Board layout Left side: SKR board attached as shown and raspberry pi and 5v supply fit overtop of the board mounted facing down to minimize room.
New Board layour Right side: With the much smaller Micro4 Fly board, the raspberry pi and 5v supply can all fit on the same plane, this shrinks the whole design signifigantly, and will make wiring much cleaner.
 <img src="https://github.com/user-attachments/assets/719a5bcc-975b-4a67-8148-b453d1f82efc" width="347"/>

  

Testing Proofs:  
-Pi zero runs klipper-mainsail without issue.  
-X, Y, Z axis all move and endstops work  
-Z axis needed 0.3amp to run reliably and not skip steps, however, would overheat to +50C in 30 seconds of running. Current solution has been to diable stepper whenever it is not moving (and due to the lead screw the axis wont fall) this has stopped overheating, as the Z-axis only runs for less than 1% of any given print.  
-Peltier module works for the bed works and heats up reliably  

Issues/Untested:  
-SSD1306 screen not tested  
-Encoder Not tested  
-Hotend not tested (but will work)  
-5v power supply not tested  
-Extruder  

