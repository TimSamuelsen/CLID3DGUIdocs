===============
Manual Controls
===============


Manual Stage Control
---------------------------
.. figure:: images/manualstagecontrol.PNG
    :align: right
    :figwidth: 300px

**Stage Select:**
Select between using SMC100CC commands or Gcode commands.
Both connections are serial, but the different motor controllers require
separate sets of commands.

**Stage Connection:**
The stage connects through serial. Select the correct COM port and click connect.

**Endstops:**
For the Gcode stage endstop can be toggled on and off. To enable endstops
select Enabled and to disable endstop select Disabled.

**Stage Position:**
Click the Get Position button to poll the stage for it's current position. 
The position is displayed in the indicator and is in units of mm.

**Absolute Move:**
Move to an absolute target position, does not take the current stage position into 
account. An absolute move to 20mm will cause the stage to move to 20mm 
regardless of it's current position. 

**Relative Move:**
Move relative to the current stage position. A relative move of 5mm will move the 
stage 5mm in the positive direction relative to it's current position. i.e  if the 
stage is at 20mm and a relative move of 5mm is executed the stage will move to 25mm.

**Stop Motion:**
Stops any moves in progress.

**Velocity:**
Sets the maximum stage velocity in units of mm/s.

**Acceleration:**
Sets the maximum stage acceleration in units of mm/s^2

**Set Position:**
For Gcode stages this sets the saved stage position, useful for zeroing the stage. 

**Min End of Run:**
Sets the lower stage position software limit ranging from -5 to 65 mm. Must be less than Max End of Run.

**Max End of Run:**
Sets the upper stage position software limit ranging from -5 to 65 mm. Must be greater than Min End of Run.

**Custom Commands:**
The user can input their own custom commands to be sent to the stage here. Useful for accessing features
that are not currently supported.

**Terminal Output:**
Provides a live readout of all operations performed in the Manual Stage Control window.

Manual Pump Control
---------------------------

.. figure:: images/manualpumpcontrol.PNG
    :align: right
    :figwidth: 300px
    
**Connect To Pump:**
The pump connects through serial. Select the correct COM port and click connect.

**Target:**
Sets the target action to perform. Setting the target to time will set the pump to inject/withdraw
for the duration of the target time. Setting the target to volume will set the pump to inject/withdraw
until it has injected/withdrawn the target volume. Once the pump has reached it's the volume or time
must be cleared before it can perform a new action.

**Active Commands:**
The Start Infusion and Start Withdraw buttons start injection/witdrawal that will run until
the pump reaches it's target. The Stop button will stop any injection/withdrawal in progress.

**Target Volume:**
The target volume to be injected/withdrawn, once started the pump will 
inject/withdraw until it reaches the target volume.

**Target Time:**
The target time for injection/withdrawal, once started the pump will 
inject/withdraw until it the target time has elapsed.

**Syringe Volume:**
Sets the syringe volume of the current syringe being used with the pump.

**Withdraw Rate:**
Sets the rate of withdrawal in units of ul/s.

**Infuse Rate:**
Sets the rate of infusion in units of ul/s.

**Custom Commands:**
The user can input their own custom commands to be sent to the pump from here. 
Useful for accessing features that are not currently supported.

**Terminal Output:**
Provides a live readout of all operations performed in the Manual Pump Control window.