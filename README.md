# ROSARIA

Type of settings and communications to use ROSARIA on mobile robots (Seekur Jr, Seekur Jr with manipulator, Pioneer 3-AT)

In our robot, we setup the communicate over Wifi (ssh coomunication). So, line number 257 is modified:
 
        n.param("port", serial_port, std::string("/dev/ttyS0"));

 
But commands changes according to the type of communications. If anyone using USB mode communication, one must modified the line number 257 with:
 
        n.param("port", serial_port, std::string("/dev/ttyS1"));  //Your USB port number "e.g, 1,2,3,4"
        
        
In this repository, we also added Sick LMS-111 laser sensor packages. The following tasks must do before use the sensor.

1. Clone or download the sick laser sensor folder.
2. Build the package using Catkin_make.
3. Setup the configuration for laser sesnor (ssh, USB).
4. Visualize the sesnor scan data in RVIZ (if you are ROS)
