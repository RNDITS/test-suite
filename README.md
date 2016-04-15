#RNDITS Test Suite
An application for evaluating the open source Geonetworking Vehicle Adapter.
Usage: 'java RnditsTestSuite' followed by any of these arguments:
```
--nocam
--nodenm
--noiclcm
--camrate <rate in Hz>
--denmrate <rate in Hz>
--iclcmrate <rate in Hz>
--receiveport <port>
--vehicleaddress <ip:port>
--stationid <id>            Station ID this application will use.
--numvehicles <num>         Number of vehicles to emulate. StationID of the other vehicles will be set as increments of 1 from the ID defined by the --stationid argument. The messages are transmitted in series. Increase the rate of CAM/DENM/iCLCM using the respective arguments to preserve the per-vehicle message rate.
```

If an option is not present, default values will be used.
Examples:
```
Start the RNDITS test suite with default options: 'java RnditsTestSuite
Without iCLCM: 'java RnditsTestSuite --noiclcm'
Without DENM and custom CAM rate: 'java RnditsTestSuite --nodenm --camrate 17'
With a custom vehicle IP: 'java RnditsTestSuite --vehicleaddress 192.168.1.19:5000'
Emulating several vehicles: 'java RnditsTestSuite --numvehicles 2 --camrate 50 --denmrate 20 --iclcmrate 50'\n"
```
