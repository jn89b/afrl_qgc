## QGC Framework
[QGC Development Design](https://dev.qgroundcontrol.com/master/en/)
Implements a Model View Controller
- [QGC Design Pattern](https://dev.qgroundcontrol.com/master/en/ui_design/) 
	- UI is written in QML -> This is the View
	- QGroundObject -> This is the Model
	- Controller is written in CPP,with QT, the buttons, commands, etc
	- 4

**HOW DO I SEND CUSTOM COMMANDS FROM QGC into Controller???**
- QGC to PX4 Drone

## PX4 Framework
- PX4 already has geofencing 
### Option 1 MAVSDK:  
- From QGC , user input values 
- From user input values MAVSDK sends to Drone 
- Drone takes message in from 
https://circuitcellar.com/research-design-hub/design-solutions/writing-mavsdk-px4-drone-applications/
- This example runs without using companion computer 


### Option 2 PX4 UORB to QGC
https://www.youtube.com/watch?v=xIu2CWedoJQ&ab_channel=AlirezaGhaderi

### Option 3 PX4 MAVROS 
https://docs.px4.io/master/en/middleware/mavlink.html
https://github.com/mavlink/mavros/issues/574
[Sending MAVROS msgs from QGC](https://github.com/mavlink/mavros/issues/1662)
https://mavlink.io/en/messages/common.html#COMMAND_LONG


### Help me
https://github.com/dronekit/dronekit-python/issues/812
https://github.com/mavlink/mavros/issues/333

https://discuss.px4.io/t/qgc-as-a-ros-node/14847

Mission Modes is the most similiar concept for PX4 not offboard
https://mavsdk.mavlink.io/v0.18.0/en/examples/fly_mission_qgc_plan.html

### Questions?
User inputs params into QGC
QGC takes these params and sends to PX4 
PX4 then takes these params and puts into flight controller

Its been done before but how to incoporate this in own custom controller?
QGC -> MAVLINK -> PX4
QGC -> MAVROS -> MAVLINK -> PX4 


### Idea 
Add ROS Plugin with QGC:
	QML -> QT that starts and launches a ros node
	Tells user what to enter
	Tells user if node is running
	Allows user to set parameters to UAV:


[QGroundControl](https://discuss.px4.io/t/is-this-possible-to-invoke-the-method-of-qgroundcontrol-from-a-django-python-web-application/17001/3) 

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6068744/pdf/sensors-18-02339.pdf