# ROSARIA

Type of settings and communication to use ROSARIA on mobile robots (Seekur Jr, Seekur Jr with manipulator, Pioneer 3-AT)

In our robot, we setup the communicate over Wifi (ssh coomunication). So, line number 257 is modified:
 
        n.param("port", serial_port, std::string("/dev/ttyS0"));

 
But commands changes according to the type of communications. If anyone using USB mode communication, one must modified the line number 257 with:
 
        n.param("port", serial_port, std::string("/dev/ttyS1"));  //Your USB port number "e.g, 1,2,3,4"
