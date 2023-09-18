# Constrained Device Application (Connected Devices)

## Lab Module 02

### Description

The **ConstrainedDeviceApp** class is the entry point of the application. This class was taken from the template which included _startApp()_, _stopApp()_ and _parseArgs()_ methods. A _main()_ method was added to the class to enable running as an application. It creates an instance of ConstrainedDeviceApp, calls _startApp()_, waits for a few seconds and then calls _stopApp()_.

The __SystemPerformanceManager__ class is created to manage and log performance tasks. pollRate is an integer attribute and locationID is a string attribute. These attributes are retrieved from ConfigUtil and used for scheduling tasks. _startManager()_ and _stopManager()_ methods are used to log the status. An instance of SystemPerformanceManager is created and managed by ConstrainedDeviceApp. The _startManager()_ and _stopManager()_ functions are connected to the _startApp()_ and _stopApp()_ functions so that it can be started and stopped with the application.

The system utility functions are abstracted into a base class __BaseSystemUtilTask__. This class has attributes _name_ and _typeID_ and corresponding getter methods. There is also a template method _getTelemetryValue()_ defined. 

The sub classes __SystemCpuUtilTask__ and __SystemMemUtilTask__ are derived from the class BaseSystemUtilTask. SystemCpuUtilTask implements the functionality to retrieve CPU utilization. While SystemMemUtilTask implements the functionality to retrieve JVM memory utilization. Both of these sub classes contain the inherited template method _getTelemetryValue()_. CPU utilization is retrieved using psutil and a float is returned in the _getTelemetryValue()_ method in SystemCpuUtilTask. JVM memory utilization is retrieved using psutil and a float is returned in the _getTelemetryValue()_ method in SystemMemUtilTask.

SystemCpuUtilTask and SystemMemUtilTask are instantiated in SystemPerformanceManager and their respective _getTelemetryValue()_ methods are invoked in a method called _handleTelemetry()_. _handleTelemetry()_ is a method defined within SystemPerformanceManager. The scheduling of the tasks is implemented using the apscheduler library.

Once all the classes were defined and connected, all the unit tests and integration tests from part01 were successfully run and passed. Hence, validating the effectiveness of the code.

### Code Repository and Branch

Repository - [piot-python-components](https://github.com/mondalso/piot-python-components.git)

Branch - [labmodule02](https://github.com/mondalso/piot-python-components/tree/labmodule02)


### UML Design Diagram(s)

This is the UML diagram depicting the classes added to the CDA workbench as part of labmodule02 and the relationship between each class.
![CDA-labmodule02](https://github.com/mondalso/book-exercise-docs/assets/124481330/fc07194e-5d3d-48f1-819e-43c5c6be8725)


### Unit Tests Executed

- src/test/python/programmingtheiot/part01/unit/common/ConfigUtilTest.py  
- src/test/python/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.py
- src/test/python/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.py

### Integration Tests Executed

- src/test/python/programmingtheiot/part01/integration/app/ConstrainedDeviceAppTest.py
- src/test/python/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.py 

EOF.
