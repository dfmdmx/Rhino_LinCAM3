# LinarandCAM 3
Rhino 6 plugin to create 2D g-code for CNC machining. 

### Color code:

Prior into opening the program you will need to assign a color to each curve depending on the desire machining preset.

 - Curve / RED, rgb (255,0,0) / Outer cut
 - Curve / BLUE, rgb (0,0,255) / Inner cut
 - Curve / GREEN, rgb (0,255,0) / Over cut
 - Curve / MAGENTA, rgb (0,255,255) / Box cut (Super beta!)
 - Point / Any color but white / Drill
 - Point / WHITE, rgb (255,255,255) / Work cero, G54
 
Every other object with difrenet color will be omitted from the selection. 

### Disclaimer:

Currently the project is under development so we recommend you update it frequently. It is not suitable for all types of CNC machines. It was developed for GRBL controllers such as Arduino and TinyG. **Its use is responsibility of the end user and we are not responsible for any direct or indirect damage that this program may cause. Hope you find it usefull.**
