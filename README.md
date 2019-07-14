# LinarandCAM 3

![alt text](https://raw.githubusercontent.com/dfmdmx/Rhino_LinarandCAM3/master/res/Icons/Logo/Rhino_LinarandCAM3_100.png)

Rhino 6 plugin to create 2D g-code for CNC machining. 

### Color code:

Prior into opening the program you will need to assign a color to each curve depending on the desire machining preset.

 <table>
 <tbody><tr><th>Objeto</th><th>Nombre Color</th><th>RGB</th><th>Rutina</th></tr><tr>
 </tr><tr><td>Curve closed</td><td>BLUE</td><td>(0,0,255)</td><td>Internal compensation</td></tr>
 <tr><td>Curve closed</td><td>RED</td><td>(255,0,0)</td><td>External compensation</td></tr>
 <tr><td>Curve closed/open</td><td>GREEN</td><td>(0,255,0)</td><td>Engraving over line</td></tr>
 <tr><td>Curve closed</td><td>MAGENTA</td><td>(0,255,255)</td><td>Box (Super beta!)</td></tr>
 <tr><td>Point</td><td>WHITE</td><td>(255,255,255)</td><td>Work cero - G54 **</td></tr>
 <tr><td>Point</td><td>Any color but white</td><td>NA</td><td>Drill</td></tr>
 </tbody>
 </table>
 
Every other object with difrenet color will be omitted from the selection. 

### Disclaimer:

Currently the project is under development so we recommend you update it frequently. It is not suitable for all types of CNC machines. It was developed for GRBL controllers such as Arduino and TinyG. **Its use is responsibility of the end user and we are not responsible for any direct or indirect damage that this program may cause. Hope you find it usefull.**
