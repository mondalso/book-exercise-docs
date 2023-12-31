# Constrained Device Application (Connected Devices)

## Lab Module 05


### Description

SystemPerformanceManager is updated to the SystemPerformanceData container and a DataUtil class is created for Json conversion.

### Code Repository and Branch

Repository - [piot-python-components](https://github.com/mondalso/piot-python-components.git)

Branch - [labmodule05](https://github.com/mondalso/piot-python-components/tree/labmodule05)

### UML Design Diagram(s)

This is the UML diagram depicting the classes added to the CDA workbench as part of labmodule02 and the relationship between each class.
![CDA-labmodule05](https://github.com/mondalso/images/blob/main/CDA-labmodule05.jpg)
[link to UML](https://github.com/mondalso/images/blob/main/CDA-labmodule05.jpg)

### Unit Tests Executed

From previous:

- src/test/python/programmingtheiot/part01/unit/common/ConfigUtilTest.py
- src/test/python/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.py
- src/test/python/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.py
- src/test/python/programmingtheiot/part02/unit/data/ActuatorDataTest.py
- src/test/python/programmingtheiot/part02/unit/data/SensorDataTest.py
- src/test/python/programmingtheiot/part02/unit/data/BaseIotDataTest.py
- src/test/python/programmingtheiot/part02/unit/data/SystemPerformanceDataTest.py
- src/test/python/programmingtheiot/part02/unit/sim/HumiditySensorSimTaskTest.py
- src/test/python/programmingtheiot/part02/unit/sim/PressureSensorSimTaskTest.py
- src/test/python/programmingtheiot/part02/unit/sim/TemperatureSensorSimTaskTest.py
- src/test/python/programmingtheiot/part02/unit/sim/HumidifierActuatorSimTaskTest.py
- src/test/python/programmingtheiot/part02/unit/sim/HvacActuatorSimTaskTest.py

New:

- src/test/python/programmingtheiot/part02/unit/sim/data/DataUtilTest.py 

### Integration Tests Executed

From previous:

- src/test/python/programmingtheiot/part01/integration/app/ConstrainedDeviceAppTest.py
- src/test/python/programmingtheiot/part02/integration/system/SensorAdapterManagerTest.py
- src/test/python/programmingtheiot/part02/integration/system/ActuatorAdapterManagerTest.py
- src/test/python/programmingtheiot/part02/integration/app/DeviceDataManagerNoCommsTest.py
- src/test/python/programmingtheiot/part02/integration/app/ConstrainedDeviceAppTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/SenseHatEmulatorQuickTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/HumidityEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/PressureEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/TemperatureEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/HumidifierEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/HvacEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/LedDisplayEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/SensorEmulatorManagerTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/ActuatorEmulatorManagerTest.py


New:

- src/test/python/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.py
- src/test/python/programmingtheiot/part02/integration/data/DataIntegrationTest.py

EOF.
