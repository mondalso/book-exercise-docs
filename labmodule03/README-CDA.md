# Constrained Device Application (Connected Devices)

## Lab Module 03

### Description

The objective of this lab module is to create classes for sensor and actuator simulation and manage the scheduling of system performance tasks, sensing tasks and actuation tasks as part of the constrained device application. There are three sensors that are being simulated, namely humidity sensor, temperature sensor and pressure sensor. Readings for each of these sensors are extracted from a dataset of values between prescribed min and max limits. There are two actuators that are being simulated, namely humidifier and hvac actuator. 

To implement the required functionality, there are a few steps that have been followed. Firstly, object classes are created to store and pass data related to sensors, actuators and system performace. Three classes are created for the same : **SensorData**, **ActuatorData** and **SystemPerformanceData**. They are all subclasses of the class **BaseIotData**. _SensorData_ is used in the class **BaseSensorSimTask** to simulate sensor telemetry values by using a randomizer. Subclasses for each of the sensors are derived from _BaseSensorSimTask_ to set appropriate boundary values in order to generate relevant telemetry. The subclasses created are **HumiditySensorSimTask**, **PressureSensorSimTask** and **TemperatureSensorSimTask**. Similarly, **BaseActuatorSimTask** is cleated to simulate the working of the actuators. Activation and deactivation methods are implemented alongside the _updateActuator_ method that uses a _ActuatorData_ class instance to pass commands to the actuator. Subclasses for each of the actuators are derived from _BaseActuatorSimTask_ in order to schedule actuator tasks. The subclasses created are **HumidifierActuatorSimTask** and **HvacActuatorSimTaskTest**. 

**SensorAdapterManager** and **ActuatorAdapterManager** classes are created to schedule sensor tasks and actuator tasks. Additonally, a **DeviceDataManager** class is also created to be able to schedule and log the tasks from **SystemPerformanceManager**, _SensorAdapterManager_ and _ActuatorAdapterManager_ simultaneously by invoking a single method. The DeviceDataManager class object is then invoked in the **ConstrainedDeviceApp** class to schedule and track system performance, sensors and actuators.

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
