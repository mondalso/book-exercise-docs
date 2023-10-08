# Constrained Device Application (Connected Devices)

## Lab Module 03

### Description

The objective of this lab module is to create classes for sensor and actuator simulation and manage the scheduling of system performance tasks, sensing tasks and actuation tasks as part of the constrained device application. There are three sensors that are being simulated, namely humidity sensor, temperature sensor and pressure sensor. There are two actuators that are being simulated, namely humidifier and hvac actuator. Readings for each of these sensors are extracted from a dataset of values between prescribed min and max limits.  

What does your implementation do? 

How does your implementation work?

### Code Repository and Branch

Repository - [piot-python-components](https://github.com/mondalso/piot-python-components.git)

Branch - [labmodule03](https://github.com/mondalso/piot-python-components/tree/labmodule03)

### UML Design Diagram(s)

This is the UML diagram depicting the classes added to the CDA workbench as part of labmodule02 and the relationship between each class.
![CDA-labmodule03](https://github.com/mondalso/images/blob/main/CDA-labmodule03.jpg)
[link to UML](https://github.com/mondalso/images/blob/main/CDA-labmodule03.jpg)


### Unit Tests Executed
From previous: 
- src/test/python/programmingtheiot/part01/unit/common/ConfigUtilTest.py  
- src/test/python/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.py
- src/test/python/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.py

New:
- src/test/python/programmingtheiot/part02/unit/data/ActuatorDataTest.py
- src/test/python/programmingtheiot/part02/unit/data/SensorDataTest.py
- src/test/python/programmingtheiot/part02/unit/data/BaseIotDataTest.py
- src/test/python/programmingtheiot/part02/unit/data/SystemPerformanceDataTest.py
- src/test/python/programmingtheiot/part02/unit/sim/HumiditySensorSimTaskTest.py
- src/test/python/programmingtheiot/part02/unit/sim/PressureSensorSimTaskTest.py
- src/test/python/programmingtheiot/part02/unit/sim/TemperatureSensorSimTaskTest.py
- src/test/python/programmingtheiot/part02/unit/sim/HumidifierActuatorSimTaskTest.py
- src/test/python/programmingtheiot/part02/unit/sim/HvacActuatorSimTaskTest.py

### Integration Tests Executed

From previous:
- src/test/python/programmingtheiot/part01/integration/app/ConstrainedDeviceAppTest.py
- src/test/python/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.py

New
- src/test/python/programmingtheiot/part02/integration/system/SensorAdapterManagerTest.py
- src/test/python/programmingtheiot/part02/integration/system/ActuatorAdapterManagerTest.py
- src/test/python/programmingtheiot/part02/integration/app/DeviceDataManagerNoCommsTest.py
- src/test/python/programmingtheiot/part02/integration/app/ConstrainedDeviceAppTest.py

EOF.
