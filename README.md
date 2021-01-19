# ntrip_ros
NTRIP client, imports RTCM streams to ROS topic

This was forked from github.com/tilk/ntrip_ros

The CORS correction server that I am using does not have the /n/r characters. So I parsed out individual messages and published each one on the /rtcm ROS topic.
It would crash with IncompleteRead error. I added patch at top of file.
But the connection had closed and it would crash again. I ended up detecting zero length data and closing and reopening the data stream.
It continues on without a glitch.

You can generate the require $GPGGA message at this site. https://www.nmeagen.org/ Set a point near where you want to run and click "Generate NMEA file". Cut and paste the $GPGGA message into the launch file.

I intend to use it with https://github.com/ros-agriculture/ublox_f9p

It may also require this package: https://github.com/tilk/rtcm_msgs

A similar NTRIP client (may be better than mine) is here: https://github.com/dayjaby/ntrip_ros
