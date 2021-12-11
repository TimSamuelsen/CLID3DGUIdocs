==============
User Interface
==============
.. image:: images/mainwindow.PNG
    :width: 1600px

Some features of the user interface are currently confidential while awaiting the 
publication of the relevant research. All print parameters, image files, and print scripts 
are stored when the GUI is closed and upon restart the GUI will initialize with the previous 
stored parameters.

Print Customization
---------------------------

.. figure:: images/ui-print-select.png
    :align: right
    :figwidth: 300px

The print customization window determines high level print features. See
Features->Print Modes to learn more.

**Select Projection Mode:**
Select between Pattern On The Fly (POTF), Video Pattern and Video mode. The printer will always initialize in
POTF mode and the light engine must be connected to properly switch projection modes.

**Select Printer:**
Select between a standard CLIP printer and other printers.

General Print Settings
---------------------------

.. figure:: images/ui-general-print-settings.PNG
    :align: right
    :figwidth: 300px
	
**Select Resin:**
Select which resin you are currently printing with. Currently this has no
effect on the print and is only stored in the print log for future reference.
Double click to edit the text field or select from a list of previously used resins.

**Bit Depth:**
Select the bit depth of your input images, the default is 1-bit
binary images. The bit depth determines how many bits the intensity of a given pixel can occupy.
Increasing the bit depth allows for more granular and detailed control of a given pixel intensity,
while also increasing the file size of a given image. In POTF mode increasing the bit depth will 
increase reupload times significantly while also lowering the max image upload. In Video Pattern 
mode every given bit depth requires separate image processing, see the Image Processing page for
more details.

A pixel with a bit depth of 1 is binary and can only be 0 or 1 corresponding to on or off. 
A pixel with bit depth 4 can have values ranging from 0000 to 1111 (0-15 in decimal) and a pixel 
with bit depth 8 can have values ranging from 0000 0000 to 1111 1111 (0-255 in decimal). 
The intensities for non-binary images(bit depth > 1) are applied after the set LED intensity. For a given pixel in a 
8 bit depth image where the LED intensity is set to 60 and the pixel intensity is 85 the resulting intensity of that
pixel will be 60 * (85/255) = 20.

**Max Image Upload:**
Determines the max number of images to upload at one time when in POTF mode, will only affect POTF mode.
With 1-bit images this caps out at 400 images, with 8-bit images this caps out at 50 images 
(can be calculated as 400/bit depth). User may want to keep the max image upload low
to avoid print discontinuities caused by long upload times.

**Starting Position:**
Simply determines the starting position of the print, this value should be at the
deadzone thickness from the window. Any movement relative to this value will be negative
each layer will move the stage closer to 0.



**Layer Thickness:**
Determines the layer thickness of the print. If set to 10 um each image file will result
in a 10um thick layer.

**Print Script:**
The print script is used to dynamically control print variables on a layer by layer basis. Print scripts should be in the format of
.txt or .csv files where each row number represents the layer number, see Dynamic Print Controls for more.


Light Engine Control
---------------------------

.. figure:: images/ui-light-engine-control.PNG
    :align: right
    :figwidth: 300px

**Initial Exposure Time:**
The initial exposure time determines the exposure time for the first layer
of the print. This allows the print to properly adhere to the build platform.
No stage movements are performed during the initial exposure.

**Exposure Time:**
Determines how long the light engine will expose for each layer.

**UV Intensity:**
Determines the intensity of the UV LEDs in the light engine (ranges from 0-255) 
where 0 = 0% LED duty cycle and 255 = 100% LED duty cycle.

**Dark time:**
Determines the time in between exposures, dark time is used for stage movement and timing overhead.



Stage Control
---------------------------
.. figure:: images/ui-stage-control.png
    :align: right
    :figwidth: 300px
	
**Print Motion Mode:**
Selects between stepped or continuous motion mode. In continuous mode the stage is
constantly in motion and in stepped mode the stage movement is paused during exposure.

**Pumping Depth:**
Pumping is an exaggerated stage movement between layers to promote resin reflow and 
avoid elastic parts sticking to the build window or deadzone.

**Stage Velocity:**
Determines the velocity of the stage. Generally does not have an active effect on the print unless set below 1 mm/s.

**Stage Acceleration:** 
Determines the acceleration of the stage. Does not have an active effect on the print unless set below 3 mm/s^2.

**Max End of Run:**
Determines the upper limit of stage movement, this value should be set to be the same height as the build window.

**Min End of Run:**
Determines the lower limit of stage movement. Default is set to 0, changing this variable is not reccommended 
unless you printing object with heights greater than max end of run.

Injection Control
---------------------------
More details to come upon publication of research.

Image Files
------------------------
.. figure:: images/ui-image-files.PNG
    :align: right
    :figwidth: 300px
	
Object image files are selected here. Make sure your image files are located in the same file and named alphabetically
the software will sort the files alphabetically as they are uploaded to the light engine.

|
|
|
|

Terminal Output
-------------------
.. figure:: images/ui-terminal-log.PNG
    :align: right
    :figwidth: 300px

**Log File Destination:**
Determines where the log file will be stored.

**Terminal Output:**
The terminal output provides a live readout of every operation performed by the software. This provides the user with insight
into the inner workings of the GUI and a valuable debug readout. Upon print completion or abort the terminal output is stored in a .txt
log with a timestamp for that print.

Active Controls
---------------------------
.. figure:: images/ui-active-control.png
    :align: right
    :figwidth: 300px

**Start Print:**
Starts the prints, must be preceded by Initialize and Synchronize and the stage must be at the correct starting position.

**Initialize and Synchronize:**
Prepares the system for your print based on your print settings and parameters. Will prompt the user to verify the print parameters
and settings. Once initialization has completed and the stage has reached the correct starting position, the print can now be started.

**Abort:**
The abort button acts as an emergency stop, click abort if something is going wrong with your print.

Peripheral Connections
---------------------------
.. figure:: images/ui-peripheral-connections.PNG
    :align: right
    :figwidth: 300px

**Light Engine:**
The light engine connects though USB HID. Click connect, if connection was succesful it should display the last error code
(usually 0), if it fails it will display "Light Engine Connection Failed" in which it failed outright or "Failed to get last error code"
in which the connection was succesful but communication is not work (in this case restart the light engine).

**Stage:**
The stage connects through RS232 serial. Select the correct COM port and click connect. To validate stage connection get the last stage position
and verify that a value is displayed.

**Pump:**
The pump connects in a similar manner to the stage. Select the correct COM port and click connect.

Popout Windows
---------------------------
.. figure:: images/ui-popout-windows.png
    :align: right
    :figwidth: 300px

**Image Processing:**
Open the image processing pop-up window. See Features->Image Processing to learn more.

**Manual Pump Control:**
Opens the manual pump control pop-up window. See Features->Manual Controls->Manual Pump Controls to learn more.

**Manual Stage Control:**
Opens the manual stage control pop-up window. See Features->Manual Controls->Manual Pump Controls to learn more.

Stage Position and Print Monitoring
------------------------------------
.. figure:: images/ui-stage-position-monitoring.png
    :align: right
    :figwidth: 300px

**Stage Position:**
The current stage position is displayed with a slider and indicator in units of mm.
It is continuously updating during the initialization and print process, the user can also
use the Get button to poll the stage for it's current position. 

**Print Monitoring:**
There are 6 possible live values from the print that can be displayed to provide the user with feedback
on which print parameters are being used or to monitor sensor inputs. Currently this is used to display
print parameters that are handled by the print script when in dynamic print mode.

Graphics Window
-----------------
The graphics window displays a graph of stage position vs. time updated throughout the print. 
It also displays the current layer of the print and the estimated remaining print time. 

.. image:: images/ui-graphics-window.png