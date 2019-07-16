# LinCAM 3

![alt text](https://raw.githubusercontent.com/dfmdmx/Rhino_LinarandCAM3/master/res/Icons/Logo/Rhino_LinCAM3_100.png)

LinCAM 3 transforms Rhino 2D geometry into cutting paths for all types of g-code based CNC machines. Its UI is mainly focused on reducing the time spend between opening the drawing and creating the g-code file, making it useful for batch production. 

### Basics

The workflow consists in three steps:

1. **LinCAM3** - This step is intended to be done once. Create a preset for each type of material with basic CAM properties such as depth, number of passes, feed, compensation, etc. This preset is linked to a specific color and type of geometry. This is considered as a fisrt setup and does not properly belongs to the workflow.

2. **Rhino** - Prepare the drawing by assigning a color to each curve depending on the desired machining job.

3. **LinCAM3**
   - Select all curves 
   - Select material (preset)
   - Select machine (postprocessor)
   - Generate g-code (write .nc file)
   - Continue to next drawing... 

This workflow allows to queue a list of drawings to be processed by the plugin in step three. We think this aproach reduces the time in the most tedious part of the manufacturing processes and opens a door into automating them.

### Color code

Prior into opening the plugin you will need to assign a color to each curve depending on the desired machining job. Every other object with different color or type of geometry will be omitted allowing for a rough selection.

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
** If no white point is selected the origin point of the drawing will be used as work cero. Using the white point is usefull only when working with multiple cut sheets in a single file. 

### Disclaimer

Currently the project is under development so we recommend you to update it frequently. It is not suitable for all types of CNC machines. It was developed for GRBL controllers such as Arduino and TinyG. It was made by the conjuction of different scripts used along the years in the workshop. So here it goes... **Its use is responsibility of the end user and we are not responsible for any direct or indirect damage that this program may cause, but mainly, we hope you find it useful!**
