# ntrip_ros for Python3 and ROS noetic
NTRIP client, imports RTCM streams to ROS topic

This Package offers a fully functional NTRIP Client for Python3 and Python2. Tested and used with the ublox f9p and hexagon smartnet.

You can generate the require $GPGGA message at this site. https://www.nmeagen.org/ Set a point near where you want to run and click "Generate NMEA file". Cut and paste the $GPGGA message into the launch file.

I intend to use it with https://github.com/ros-agriculture/ublox_f9p

It requires this package: https://github.com/tilk/rtcm_msgs
