*************************
Dynamic Print Controls
*************************

.. contents:: Table of Contents

Print Script
=============
The print script is used to dynamically control print parameters on a layer by layer basis. The print script is a comma-separated values
(.csv) file that can be generated either with excel, text editors or with a custom script.


30 μm CLIP printer
---------------------------

The 30 μm printer can control the exposure time (ms), LED intensity, and dark time (ms) as dynamic variables. 
An example print script is included on the left side below with exposure time values ranging from 11-20, 
LED intensity values ranging from 21-30 and dark time ranging from 31-40. The example print script was generated in
Excel and saved as a .csv file, the image below on the right side displays the example table in excel.

.. list-table:: Print Script Order and Units
   :widths: 12 12 12 12 12 12 12
   :header-rows: 1

   * - Exposure Time
     - LED Intensity
     - Dark Time
     - Layer Thickness
     - Stage Velocity
     - Stage Acceleration
     - Pump Height
   * - ms
     - 1-255
     - ms
     - μm
     - mm/s
     - mm/s^2
     - μm

.. |logo1| image:: https://i.imgur.com/UB2vqhL.png
    :scale: 60%

.. |logo2| image:: https://i.imgur.com/J1b4koi.png
    :scale: 60%

.. table:: 30 μm CLIP print script (exp time, LED intensity, dark time)
   :align: center

   +---------+---------+
   | |logo1| | |logo2| |
   +---------+---------+

iCLIP printer
---------------------------
The iCLIP printer can control the exposure time (ms), LED intensity, dark time (ms), injection volume per layer
(μl), and injection rate (μl/s) as dynamic variables. 
An example print script is included on the left side below with the exposure time values ranging from 11-20, 
LED intensity values ranging from 21-30, dark time ranging from 31-40, injection volume ranging from 41-50, 
and injection rate ranging from 51-60. The example print script was generated in
Excel and saved as a .csv file, the image below on the right side displays the example table in excel.

.. list-table:: Print Script Order and Units
   :widths: 12 12 12 12 12 12 12 12 12
   :header-rows: 1

   * - Exposure Time
     - LED Intensity
     - Dark Time
     - Layer Thickness
     - Stage Velocity
     - Stage Acceleration
     - Pump Height
     - Injection Vol.
     - Injection Rate
   * - ms
     - 1-255
     - ms
     - μm
     - mm/s
     - mm/s^2
     - μm
     - μl
     - μl/s

.. |logo3| image:: https://i.imgur.com/pHoKDPa.png
    :scale: 60%

.. |logo4| image:: https://i.imgur.com/1I76b2v.png
    :scale: 60%

.. table:: iCLIP print script (exp time, LED intensity, dark time, inj vol, inj rate)
   :align: center

   +---------+---------+
   | |logo3| | |logo4| |
   +---------+---------+


