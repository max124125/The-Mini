
<p float="left">
  <img src="https://github.com/user-attachments/assets/053dbf47-2d4c-473e-b85b-c99c70d783e3" width="350" />
  <img src="https://github.com/user-attachments/assets/052ca413-d359-4bd2-86f1-8dcd0c32871f" width="347"/>

</p>

# The-Mini
The smallest - yet still fully functional - 3D printer I could design.    

Design goals:  
-Other smaller printers of this size used ROM drive steppers. I have oppted to exclude these for the x and y axes as they have very limited accuracy (20steps/mm) compared to traditional Nema 14 based printers (80steps/mm).  
-An additional goal is for this printer to be able to achieve the same speed/accel of a default ender 3 (500mm/s2 at 50mm/s).  
-The entire printer (excluding filament and power supply) needs to fit into the 3x4x5 inch Vaultz lockbox I have (see image).

Current updates: 
-The release of the new Micro4 fly board by Mellow has led to a full rebuild of the printer. This is due to the major space savings from the new board. With the older SKR board, the printer was very close to not fitting in the vaultz box (actually tearing some of the fabric, and being hard to close due to the tight fit). But with the new board the printer could easily be up to 5mm shorter, and 10mm thinner. This will hopefully give a lot cleaner of a fit and even allow the addition of a small power supply or filament roll the fit in the box with the printer. 

New Board layout below:
Old SKR board on the left (raspberry pi and 5v supply fit overtop of the board), Micro4 Fly board on the bottom right (even with the pi above and 5v supply they are combined smaller)
 <img src="https://github.com/user-attachments/assets/719a5bcc-975b-4a67-8148-b453d1f82efc" width="347"/>



Software Proofs:
-Pi zero runs klipper-mainsail without issue.
-X, Y , Z axis all move and endstops work
-Z axis needed 0.3amp to run reliably and not skip steps, however, would overheat to +50C in 30 seconds of running. Current solution has been to diable stepper whenever it is not moving (and due to the lead screw it wont move) this has stopped overheating, as the Z-axis only runs for less than 1% of any given print.
-Peltier module works for the bed works and heats up reliably

Issues/Untested:
-SSD1306 screen not tested

