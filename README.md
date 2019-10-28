Jacob Engelbrecht

October 29, 2019 

Professor Lee

Modern Robotic Programming


# URDF Lab 5

## How to Run 
For the complete model to be shown and stable, several steps need to occur. 

### Run RVIZ with new IMU model 
To display the RVIZ containing the new base link in addition to the IMU, launch:
> lab5.launch use_xacro:=true

Now the new links can be seen but the robot appears the same. 

### RVIZ Preview with Lab 4 Model
To launch the simulation prior to IMU addition, the following needs to be run: 
> display.launch use_xacro:=true 

This will launch RVIZ showing the robot. The arg is not necessary, but the complete robot will not be shown unless the xacro is enabled. 
This requires the complete the complete repo to be downloaded, as the RVIZ configuration file is loaded. (Note the blue color :)

### Joint State Publisher 
There are two options for configuring the joints

#### Using the GUI 
If a gui is desired to configure the joint states, simply one more arg needs to be passed to the launch file. 
> display.launch use_xacro:=true use_gui:=true


#### Using Static Publishers 
If status transforms are desired, the default launch file can be run. 

## Issues 
There were some issues I ran into while completeling this lab. 

### Axes
I had a difficult time having the wheels rotate correctly. I figured out that the issue was related to the axis, which I somewhat resolved.
The wheels now spin with the correct degrees of freedom, but I am not able to center the axis roation with the larger wheels. 

### Warnings 
Additionally, if the .xacro file is run on melodic, a warning is thrown due to in order processing is now the norm. 
