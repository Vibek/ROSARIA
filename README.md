# ROSARIA

NOTE: In my robot, we setup wifi to communicate. so, line number 257 is modified:
 n.param( "port", serial_port, std::string("/dev/ttyS0") );
 
 But if someone use usb port in order to communicate, line number should be modified with:
  n.param( "port", serial_port, std::string("/dev/ttyS1") ); //Your USB port number "e.g, 1,2,3,4"
