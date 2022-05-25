# QGroundControl Development
- Go with plugin architecture:
- https://dev.qgroundcontrol.com/master/en/custom_build/Plugins.html

**QGC PLugin**
https://github.com/mavlink/qgroundcontrol/blob/master/src/api/QGCCorePlugin.cc

**Autopilotplugin**
https://github.com/mavlink/qgroundcontrol/blob/master/src/AutoPilotPlugins/AutoPilotPlugin.h

Example
https://github.com/jn89b/afrl_qgc/tree/master/custom-example/src

https://dev.qgroundcontrol.com/master/en/custom_build/custom_build.html

In res directory:
Have QML files -> markup language like HTML/CSS, incoporates JavaScript for any functions to be applied 

In src:
Have cpp header and source files


# LQR  
- Plan on submitting paper for AIAA in GNC and competition 
# MOCAP Drone
- Got data into into MAVROS, z-axis off so need to check or reflash hardware

# AFRL QGC
## Scenarios
- From discussion created user stories -> acceptance criteria
- User stories:
	- As a user I want to.. so that I can 
- Acceptance Criteria:
	- Given ... When .... Then

## Software Architecture:
- Pull from main repo:
	- This is the main repo:
- Custom build repo: 
	- Changes are made in this repo
- Utilize custom plugin architectures, inherit from these classes and extend code without breaking it
	- FirmwarePlugin
	- AutopilotPlugin
	- QGCCorePlugin 
- Probably place controller in autopilot plugin 
- QGCCorePlugin 

## Gameplan: 
- Develop prototype mockuip:
	- From mock digital card -> send information to QGC and QGC tells autopilot to do something or say message recieved:
	- Use MAVSDK or MAVROS protocol
- Break down user stories and figure out my sprints to complete
- Develop wireframe of layout 
- Finish each sprint iteratively and test
- Testing protocol are as follows:
	- Test with HITL with gazebo for FW applications 
	- Once good test in real life  




