# Constrained Device Application (Connected Devices)

## Lab Module 04

### Description

In the previous lab module, the sensors and actuators were simulated. The objective of this lab module is to perform similar tasks but by emulating the sensors and actuators. Classes for sensor and actuator emulation are created and called by the the sensing and actuation task managers as part of the constrained device application. There are three sensors that are being emulated, namely humidity sensor, temperature sensor and pressure sensor. Readings for each of these sensors are extracted from the SenseHat emulator. There are three actuators that are being simulated, namely humidifier, hvac actuator and LED actuator. 

To implement the required functionality, there are a few steps that have been followed. Firstly, the Sense-Emu Sense HAT emulator needs to be installed and configured by installing Sense-Emu and pisense python libraries. Then the object classes for emulating sensor data must be derived from _**BaseSensorSimTask**_. Three classes are created for the same : _**HumiditySensorEmulatorTask**_, _**PressureSensorEmulatorTask**_ and _**TemperatureSensorEmulatorTask**_. The sensor readings are extracted from the SenseHat emulator using the _generateTelemetry_ method in each of these classes. Similarly, object classes are created for emulating actuator tasks. Three classes are derived from _**BaseActuatorSimTask**_ for the same : _**HumidifierEmulatorTask**_, _**HvacEmulatorTask**_ and _**LedDisplayEmulatorTask**_. The respective activation and deactivation methods are implemented in each of these classes.  Finally, _**SensorAdapterManager**_ and _**ActuatorAdapterManager**_ are updated to include the implementation of the emulation data alongside the previously implemented simulation data.

### Code Repository and Branch

Repository - [piot-python-components](https://github.com/mondalso/piot-python-components.git)

Branch - [labmodule04](https://github.com/mondalso/piot-python-components/tree/labmodule04)

### UML Design Diagram(s)

This is the UML diagram depicting the classes added to the CDA workbench as part of labmodule02 and the relationship between each class.
![CDA-labmodule04](https://github.com/mondalso/images/blob/main/CDA-labmodule04.jpg)
[link to UML](https://github.com/mondalso/images/blob/main/CDA-labmodule04.jpg)


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



### Integration Tests Executed

From previous:
- src/test/python/programmingtheiot/part01/integration/app/ConstrainedDeviceAppTest.py
- src/test/python/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.py
- src/test/python/programmingtheiot/part02/integration/system/SensorAdapterManagerTest.py
- src/test/python/programmingtheiot/part02/integration/system/ActuatorAdapterManagerTest.py
- src/test/python/programmingtheiot/part02/integration/app/DeviceDataManagerNoCommsTest.py
- src/test/python/programmingtheiot/part02/integration/app/ConstrainedDeviceAppTest.py

New:
- src/test/python/programmingtheiot/part02/integration/emulated/SenseHatEmulatorQuickTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/HumidityEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/PressureEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/TemperatureEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/HumidifierEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/HvacEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/LedDisplayEmulatorTaskTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/SensorEmulatorManagerTest.py
- src/test/python/programmingtheiot/part02/integration/emulated/ActuatorEmulatorManagerTest.py

EOF.
