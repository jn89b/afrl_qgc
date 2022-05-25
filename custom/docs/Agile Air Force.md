# Software Design for AFRL
[Agile Development](https://www.cprime.com/resources/what-is-agile-what-is-scrum/#:~:text=.-,User%20Story)

#### Module 1: Performance
**This is basically V-N Diagram**
##### User Wants to see Power VS Airspeed
**User Story**
- As a user I want to be able to see the Power required versus airspeed so that I can evaluate the performance of my aircraft 

##### User Wants to see Power AVAILIBLE VS Airspeed
**User Story**
- As a user I want to be able to see Power availible versus airspeed so that I can evaluate the limitations of my aircraft

##### User Wants to see Range VS Airspeed
**User Story**
- As a user I want to be able to see the Range versus airspeed plot so that I can understand the relationship between those two in my Aircraft

##### User Wants to see Endurance VS Airspeed
**User Story**
- As a user I want to be able to see the maximum endurance, maximum endurance airspeed versus to know the endurance performance of my aircraft

##### User Wants to see Drag and Glide Polar
**User Story**
- As a user I want to be able to see the drag and glide polar so that I can know the characteristics of my aircraft 

##### Supervised Flight Controller -> Idiot Check
**Checkout 3.2.1**
**User Story** 
[Flight Envelope](http://www.aerodynamics4students.com/aircraft-performance/flight-envelope.php)
[Flight Envelope 2](http://www.aviationchief.com/operating-flight-strength-v-g--v-n-diagrams.html)
- As a user I want to be ensured that the flight control will make sure that my aircraft will maintain safe flight, so that when I command a specific manuver the aircraft will not crash

##### Questions 
- How to derive this VN?
- How does the control law know its limitations, without this? 

#### Module 2: Flight Dynamics
##### User wants to command inputs
- As a user I want to be able to input pulses, frequency sweeps, and multisines to the system so that I can collect data 

##### User wants to see the response in the QGC in time and Z domain
- As a user I want to see in the GUI the closed loop response of the system in the time and z-domain so that I can analyze the control response

##### User wants to tune the system 
- As a user I want to be able to tune the system in the inner and outer loop to see the closed loop responses of the system and see the stability margins

##### Questions 
- The user is allowed to adjust the gains real time during mission deployment?
- Think its better to know before hand the limitations 
- Also if user enters stupid values into system automatically, deny the values, instead of requiring the user to hit a knock-it-off button to mitigate any risks 

#### Modules 3: Mission Systems
##### User wants to see airframe gimbal camera
- As a user I want to see the camera from the aircraft in my ground station for visual surveillance of the area around me 

##### User wants to see Aircraft through LIDAR
- As a user I want to be able to see the LIDAR data so that I can map the around me 

##### User wants Aircraft to recognize/detect objects
- As a user I want to be able to detect objects in my aircraft so that I can plan and strategize accordingly based on the classifications 


# Splitting it up

## Flight Control Software Coupled with QGC
##### User wants to see Flight Envelope 
###### User Wants to see Power VS Airspeed
**User Story**
- As a user I want to be able to see the Power required versus airspeed so that I can evaluate the performance of my aircraft 

###### User Wants to see Power AVAILIBLE VS Airspeed
**User Story**
- As a user I want to be able to see Power availible versus airspeed so that I can evaluate the limitations of my aircraft

###### User Wants to see Range VS Airspeed
**User Story**
- As a user I want to be able to see the Range versus airspeed plot so that I can understand the relationship between those two in my Aircraft

###### User Wants to see Endurance VS Airspeed
**User Story**
- As a user I want to be able to see the maximum endurance, maximum endurance airspeed versus to know the endurance performance of my aircraft

###### User Wants to see Drag and Glide Polar
**User Story**
- As a user I want to be able to see the drag and glide polar so that I can know the characteristics of my aircraft 

##### User wants to tune the system 
- As a user I want to be able to tune the system in the inner and outer loop to see the closed loop responses of the system and see the stability margins

##### User wants to command inputs
- As a user I want to be able to input pulses, frequency sweeps, and multisines to the system so that I can collect data

##### Admin Idiot Check
- As an admin, I want to define constraints for the user based on the inputs, to prevent users from harming the aircraft

##### Automated Idiot Check
- I want to check if inputs from the user "make" sense, if not prevent the users from doing so

##### User wants to define performance control -> Limited by the Idiot Check
- As a user I want to be able to set throttle, airspeed, and bank angle commands for specified times to evlaluate the performance limits of my aircraft 

##### User wants to see airframe gimbal camera
- As a user I want to see the camera from the aircraft in my ground station for visual surveillance of the area around me 

##### User wants to see Aircraft through LIDAR
- As a user I want to be able to see the LIDAR data so that I can map the around me 

##### User wants Aircraft to recognize/detect objects
- As a user I want to be able to detect objects in my aircraft so that I can plan and strategize accordingly based on the classifications 

## Flight Controller Only 
##### Supervised Flight Controller -> Idiot Check
**Checkout 3.2.1**
**User Story** 
[Flight Envelope](http://www.aerodynamics4students.com/aircraft-performance/flight-envelope.php)
[Flight Envelope 2](http://www.aviationchief.com/operating-flight-strength-v-g--v-n-diagrams.html)
- As a user I want to be ensured that the flight control will make sure that my aircraft will maintain safe flight, so that when I command a specific manuver the aircraft will not crash

## Ground Control Station Only
##### User wants digital flight card test for information collection
- As a user I want to be able to see the history of the flight and performance of the UAS, during this flight test manuever
- Ascent:
	- Set throttle whatever
	- Set angle whatever

##### User wants to see the response in the QGC in time and Z domain
- As a user I want to see in the GUI the closed loop response of the system in the time and z-domain so that I can analyze the control response


## Visual Plots
- UI: 
- Strip charts: 
- Subplots 
- Command, response 
- Airspeed roll pitch command 


## SuperVisory Control Law 
- Test Config 
	- Geofencing 
	- Airspeed limits 
	- Attitude limits 
- Aircraft + Area will dictate the control law 


## Example of Aircraft Test
- Objectives of test:
	- Develop the glide polar 
	- Assess the dynamic response 
- Given run way
	- Climb to some height
	- Back and forth between waypoints
	- During transition add inputs specified by user
	- RTL protocol 


