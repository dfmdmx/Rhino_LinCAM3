# LinarandCAM 3

![alt text](https://raw.githubusercontent.com/dfmdmx/Rhino_LinarandCAM3/master/res/Icons/Logo/Rhino_LinarandCAM3_100.png)

LinarandCAM 3 converts Rhino 2D geometry into cutting paths for all types of g-code based CNC machines. Its UI is mainly focused on reducing the time spend between opening the drawing and creating the g-code file, making it usefull for batch production. 

### Basics

The workflow consists in three steps. The fisrt two are done outside the plugin, allowing the workflow to queue a list of drawings waiting for g-code processing made by the plug-in in step 3. 

1. Prepare the drawing - Involves assigning a color to each curve
2. Create a preset for each type of material with basic CAM properties such as depth, number of passes, feed, compensation, etc. that are linked to a specific color and type of geometry. (This is done inside the plugin, but once, so we dont add this setup time into the workflow.)

3. Open LinarandCAM3 - Select all curves - Select material - Select machine - Generate g-code - Continue to next drawing...

### Color code:

Prior into opening the program you will need to assign a color to each curve depending on the desire machining job.

 <table>
 <tbody><tr><th>Object</th><th>Color name</th><th>RGB</th><th>Machining job</th></tr><tr>
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
