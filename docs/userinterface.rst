==============
User Interface
==============
.. image:: images/mainwindow.JPG
    :width: 1600px

Print Customization
---------------------------

.. figure:: https://i.imgur.com/N3GkRIh.png
    :align: right
    :figwidth: 300px

The print customization window determines high level print features. See
Features->Print Modes to learn more.

**Select Resin:**
Currently not in use.

**Select Projection Mode:**
Select between Pattern On The Fly (POTF) and video pattern mode.

**Select Printer:**
Select between a standard CLIP printer and DI-CLIP printer.

**Print Type:**
Select between stepped or continuous motion.

**Bit Depth:**
Select the bit depth of your input images, the default is 1-bit
binary images. Increasing the bit depth allows for varying depths of
grayscale up to 8-bit grayscale images.

**Max Image Upload:**
Determines the max number of images to upload at one time when in POTF
mode. With 1-bit images this caps out at 400 images, with 8-bit images
this caps out at 50 images. User may want to keep the max image upload low
to avoid print discontinuities caused by long upload times.

General Print Settings
---------------------------

.. figure:: https://i.imgur.com/sptkfoX.png
    :align: right
    :figwidth: 300px

**Initial Exposure Time:**
The initial exposure time determines the exposure time for the first layer
of the print. This allows the print to properly adhere to the build platform.

**Starting Position:**
Simply determines the starting position of the print, this value should be at the
deadzone thickness from the window. Any movement relative to this value will be negative
each layer will move the stage closer to 0.

**Slice Thickness:**
Determines the layer thickness of the print. If set to 10 um each image file will result
in a 10um thick layer.

**Auto Mode Settings:**
Determines print settings automatically based on desired print speed and height. Not in much use
at the moment.

**Light Engine Control:**

* Exposure time determines how long the light engine will expose for each layer. If a print script is active it will take over exposure time control.
* UV Intensity determines the intensity of the UV LEDs in the light engine (ranges from 1-255).
* Dark time determines the time in between exposures, dark time is used for stage movement and timing overhead.

**Stage Control:**

* Stage velocity determines the velocity of the stage. Does not have an active effect on the print unless set below 1 mm/s.
* Stage acceleration determines the acceleration of the stage. Does not have an active effect on the print unless set below 3 mm/s^2.
* Max end of run determines the upper limit of stage movement, this value should be set to be the same height as the build window.
* Min end of run determines the lower limit of stage movement. Default is set to 0, changing this variable is not reccommended unless you printing object with heights greater than max end of run.

**Pump Control:**
Pump control is currently not in use.

Peripheral Controls
---------------------------
.. figure:: https://i.imgur.com/CBlX0mU.png
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
The pump connects in a similar manner to the stage. Select the correct COM port and click connect. The pump is not currently in use.

Input Files
---------------------------
.. figure:: https://i.imgur.com/V4CLCEd.png
    :align: right
    :figwidth: 300px

**Image Files:**
Object image files are selected here. Make sure your image files are located in the same file and named alphabetically
the software will sort the files alphabetically as they are uploaded to the light engine.

**Print Script:**
The print script is used to dynamically control print variables on a layer by layer basis. Print scripts should be in the format of
.txt or .csv files where each row number represents the layer number and consists of: [Exposure time in us,  UV Intensity,].

Print Controls
---------------------------
.. figure:: https://i.imgur.com/Nz9QY79.png
    :align: right
    :figwidth: 300px

**Start Print:**
Starts the prints, must be preceded by Initialize and Synchronize and the stage must be at the correct starting position.

**Initialize and Synchronize:**
Prepares the system for your print based on your print settings and parameters. Will prompt the user to verify the print parameters
and settings. Once initialization has completed and the stage has reached the correct starting position, the print can now be started.

**Abort:**
The abort button acts as an emergency stop, click abort if something is going wrong with your print.

**Image Processing:**
Open the image processing pop-up window. See Features->Image Processing to learn more.

**Manual Pump Control:**
Opens the manual pump control pop-up window. See Features->Manual Controls->Manual Pump Controls to learn more.

**Manual Stage Control:**
Opens the manual stage control pop-up window. See Features->Manual Controls->Manual Pump Controls to learn more.


Print Log
-------------------
.. figure:: https://i.imgur.com/qYGeweg.png
    :align: right
    :figwidth: 300px

**Terminal Output:**
The terminal output provides a live readout of every operation performed by the software. This provides the user with insight
into the inner workings of the GUI and a valuable debug readout. Upon print completion or abort the terminal output is stored in a .txt
log with a timestamp for that print.

**Log File Destination:**
Determines where the log file will be stored.

Print Monitoring
---------------------------

**Graphics Window:**

**Current Stage Position:**

**Monitor Live Values:**
