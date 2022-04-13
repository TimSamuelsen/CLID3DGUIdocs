============
History
============
The project was in the prototyping phase from 01/17/2021-03/24/2021.

0.1.0 (2021-03-24)
------------------

* **NEW:** First implementation of a fully functioning print process.

0.1.1 (2017-04-02)
~~~~~~~~~~~~~~~~~~

* **NEW:**  Added initial exposure time and proper reupload
* **FIX:** Stage velocity issue.
* **IMPROVED:** Redesigned UI

0.1.2 (2021-04-12)
~~~~~~~~~~~~~~~~~~

* **NEW:** Manual Pump Control window and library, user can now select image reupload limit, implemented confirmation screen
* **FIX:**  Fix on stop button in manual stage control
* **IMPROVED:** Graphics Window

0.1.3 (2021-04-22)
~~~~~~~~~~~~~~~~~~~

* **NEW:** Print Script for dynamic prints, auto parameter calculations
* **FIX:**  Intermittent crashes caused by problems with serial communication library
* **IMPROVED:** Revamped serial communication, improved stage lowering

0.1.4 (2021-05-14)
~~~~~~~~~~~~~~~~~~~

* **NEW:** image processing window with working encoding algorithm, image popout window for video pattern mode
* **FIX:**  Fixed linking issues for .dll files, video pattern mode artifact solved

0.1.5 (2021-05-26)
~~~~~~~~~~~~~~~~~~~

* **NEW:** LED Intensity is now in print script, bit depth selection to enable grayscale, continuous motion print mode
* **IMPROVED:** Image popout window now automatically opens in the extended desktop in fullscreen.

0.1.6 (2021-06-04)
~~~~~~~~~~~~~~~~~~~

* **NEW:** Pumping mode added as high level print control variable

0.2 (2021-06-11)
------------------

* **NEW:** First implementation of Video Pattern mode
* **FIX:**  Reupload issue and timer drift issue when in pumping mode
* **IMPROVED:** Comments

0.3 (2021-06-25)
------------------

* **NEW:** Second printer support, GCode stage support

0.3.1 (2021-07-01)
~~~~~~~~~~~~~~~~~~~

* **NEW:** Continuous injection mode
* **IMPROVED:** Added dark time, injection rate, and injection volume to supported dynamic variables

0.3.2 (2021-07-17)
~~~~~~~~~~~~~~~~~~~

* **NEW:** Pre and post stage movement injection delay, first attempt at vp8bit workaround
* **FIX:** Initial exposure time bug, intermittent crash issue was fixed by reverting layerCount variable back to uint
* **IMPROVED:** Added stage velocity, stage acceleration, pump height, and layer thickness to supported dynamic variables

0.4 (2021-08-01)
-------------------
* **NEW:** Redesigned UI for mainwindow, image processing, manual stage and pump control
* **IMPROVED:** Organized most module level variables into data structures for print settings, print controls, print scripts etc.


0.4.1 (2021-08-14)
~~~~~~~~~~~~~~~~~~~
* **NEW:** Revised system arcitecture, increasing program modularity
* **IMPROVED:** Removed all access to mainwindow from other modules, leaned into the signal and slots approach in Qt to handle errors messages and terminal

0.4.2 (2021-08-25)
~~~~~~~~~~~~~~~~~~~
* **NEW:** Redesigned software now working on 30 um printer, Added doxygen + breathe integration for documentation 
* **FIX:** Stage position feedback, video pattern in dynamic mode crashing issues 
* **IMPROVED:** Serial connection pass through from manual control windows, add pattern function reworked

0.4.3 (2021-09-21)
~~~~~~~~~~~~~~~~~~~~
* **NEW:** Revamped print logs, print titles and resin selection now logged, stepped continuous injection
* **FIX:** First layer intensity with print script now set correctly, no longer crashes with print script and no images
* **IMPROVED:** Positional feedback update frequency increased
  
0.5 (2021-10-11)
~~~~~~~~~~~~~~~~~~~~
* **NEW:** Video mode implemented
* **IMPROVED:** Split out graphics, print script handling, printcontrols into separate classes and .ui files

0.5.1 (2021-10-26)
~~~~~~~~~~~~~~~~~~~~
* **NEW:** Pixel binning added to image processing, post exposure delay
* **FIX:** Image scaling crashing issue resolved
* **IMPROVED:** Split out print settings toolbox into separate class and .ui files, reconfigured ui to use Qt native layouts

0.6 (2021-11-10)
~~~~~~~~~~~~~~~~~~~~
* **NEW:** Pattern repeating for video pattern mode, jerk time parameter, 
* **FIX:** Stage initialization hanging

0.6.1 (2021-11-16)
~~~~~~~~~~~~~~~~~~~~
* **NEW:** Initial attempt of adding Thorcam API and creating focus calibration window

0.7 (2021-12-9)
~~~~~~~~~~~~~~~~~~~~
* **NEW:** Storing of images and print script upon closing window, reset button
* **IMPROVED:** Image buffer reading of ThorCam images

0.7.1 (2022-2-8)
~~~~~~~~~~~~~~~~~~~~
* **NEW:** New stage initialization protocol
* **IMPROVED:** Cleaned up DLP9000 API and mainwindow source code, updated print control and print commmands

1.0 (2022-3-23) Final Commit Tim
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* **NEW:** Auto connection to peripherals and initialization of light engine upon startup
* **FIX:** Initial exposure bug
* **IMPROVED:** Added code formatting (customized Google C++ standards), cleaned up SMC100CC API