Copy "sensor_imx335_mipi.ko" to /root/ and "imx335fpv.bin" to /etc/sensors/

Run:
rmmod sensor_imx335_mipi

insmod /root/sensor_imx335_mipi.ko chmap=1

killall -1 majestic

Set : "sensorConfig: /etc/sensors/imx335fpv.bin" in majestic.yaml

Exposure can be set to 1 during day for higher FPS.

Stabile modes for ssc30kq:
1) Sensor cropped to 2560x1440 ( 16:9 ) 60 fps - set resolution to 1920x1080 ( max resolution 2560x1440 )
2) Sensor cropped to 2560x1440 ( 16:9 ) 80 fps - set resolution to 1920x1080 ( max resolution 2240x1260 )
3) Sensor cropped to 2240x1260 100fps - set resolution to 1920x1080 ( max resolution 1920x1080 )
4) Sensor cropped to 1920x1080 120fps ( real 117fps ) - set resolution to 1600x900 ( max resolution 1920x1080 )

Use recommended resolution for each mode with SSC30KQ, with max resolution there are encoding glitches if active cooling is not used. If image has glitches, set lower resolution or lower fps in majestic settings.

   
