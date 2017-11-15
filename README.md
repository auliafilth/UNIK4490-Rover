# UNIK4490-Rover
<img src="https://github.com/KvalheimRacing/UNIK4490-Rover/blob/master/Rover_2/rover_pic.PNG" width="400" height="340">

> 4 by 4 rover project

This is a joint collaboration between two groups studying [*UNIK4490 - Control of manipulators and mobile robots*](http://www.uio.no/studier/emner/matnat/its/UNIK4490/index-eng.html) at the University of Oslo.
In this project we are implementing controllers for path planning and velocity control of each wheel.

##### Known hardware on the rover;
| Name | Description |
| ----- | ---- |
|Hsiang Neng - hn-gh12-1634t 200rpm 30:1 geared |motor with encoder|
|Intel Nuc |computer|
|Some unknown teensy version| small arduino board for reading encoder data|

The folder "Rover_1" contains all software for the rover without lidar, and the folder "Rover_2" contains the software for the rover with lidar


#### Other useful information (pending)
- Rover 2 has wifi (pwd now retrieved Martin has connected through ssh
- All encoders on rover 1 is working (although unstable usb), there is a teensy for reading the values (rover 2 has the same setup, but not tested)
- The motor driver on each rover controls both wheel at one side at the same time (meaning you control either left or right wheels)
- driver_pid.py works now, sometimes the usb plug just need to be taken in and out
-driver_pid.py needs to be modified to send out the correct velocities on the topic /est_vel. The correct velocities is commented out and is laying on rover 1 now.
- modified driver.py (that worked), to include driving the wheels on both sides and reading encoder data. driver.py needs further to listen to the topic /cmd_vel and assign speeds based on that (or one can fix driver_pid.py).
- [uio repo](https://github.uio.no/UNIK4490/rover_setup)
