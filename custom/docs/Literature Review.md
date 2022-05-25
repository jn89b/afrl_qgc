## [Extending QGroundControl for Automated Mission Planning of UAVs](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6068744/pdf/sensors-18-02339.pdf)
### What is this Paper about?
- Extended QGC for fliht control of multiple vehicles, and allows operator to do "complex" tasks 
- Gives a guide on how to do this, code is confidential
![[Pasted image 20220523140122.png]]
### How did they do it?
- Added a new tab to extend new missions, modified QGC source code

### What are the Features? 
- New Missions 
	- Define name of mission 
	- Define bounds of mission 
	- Define arc-seconds of the elevation of map 
	- Start time as option or use CPU clcok
- Add UAV
	- Define name of UAV
	- The initial amount of fuel or battery left of UAV 
	- The position of UAV
	- Optional inputs:
		- End position for depature of runway
		- Optional start position for landing 
		- Optional end position of UAV for landing
		- Optional start and end times of UAV 
		- Type of UAV
- Add GCS
	- Name of GCS
	- Position of GCS
	- Type of GCS
		- Range of communication 
		- Maximum number of vehicles 
		- Type of vehicles,
		- Draws an orange circle and shows the radius and range of GCS
![[Pasted image 20220523140757.png]]