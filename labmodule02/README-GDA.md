# Gateway Device Application (Connected Devices)

## Lab Module 02

### Description

The **GatewayDeviceApp** class is the entry point of the application. This class was taken from the template which included _startApp()_, _stopApp()_ and _parseArgs()_ methods. A _main()_ method was added to the class to enable running as an application. It creates an instance of GatewayDeviceApp, calls _startApp()_, waits for a few seconds and then calls _stopApp()_.

The __SystemPerformanceManager__ class is created to manage and log performance tasks. pollRate is an integer attribute that is retrieved from ConfigUtil and used for scheduling tasks. _startManager()_ and _stopManager()_ methods are used to log the status. An instance of SystemPerformanceManager is created and managed by GatewayDeviceApp. The _startManager()_ and _stopManager()_ functions are connected to the _startApp()_ and _stopApp()_ functions so that it can be started and stopped with the application.

The system utility functions are abstracted into a base class __BaseSystemUtilTask__. This class has attributes _name_ and _typeID_ and corresponding getter methods. There is also an abstract template _getTelemetryValue()_ is defined. 

The sub classes __SystemCpuUtilTask__ and __SystemMemUtilTask__ are derived from the class BaseSystemUtilTask. SystemCpuUtilTask implements the functionality to retrieve CPU utilization. While SystemMemUtilTask implements the functionality to retrieve JVM memory utilization. Both of these sub classes contain the inherited template method _getTelemetryValue()_. It retrieves the CPU utilization in SystemCpuUtilTask and returns the value as a float. It retrieves the JVM memory utilization in SystemMemUtilTask and returns the value as a float. 

SystemCpuUtilTask and SystemMemUtilTask are instantiated in SystemPerformanceManager and their respective _getTelemetryValue()_ methods are invoked in a method called _handleTelemetry()_. _handleTelemetry()_ is a method defined within SystemPerformanceManager with a scheduler service that handles interval-based calls to retrieve each task's value.

Once all the classes were defined and connected, all the unit tests and integration tests from part01 were successfully run and passed. Hence, validating the effectiveness of the code.

### Code Repository and Branch

Repository - [piot-java-components](https://github.com/mondalso/piot-java-components.git)

Branch - [labmodule02](https://github.com/mondalso/piot-java-components/tree/labmodule02)

### UML Design Diagram(s)

This is the UML diagram depicting the classes added to the GDA workbench as part of labmodule02 and the relationship between each class.
![GDA-labmodule02](https://github.com/mondalso/book-exercise-docs/assets/124481330/e94a402f-c6af-41e3-801a-34c8aa905c01)
[link to UML](https://github.com/mondalso/book-exercise-docs/assets/124481330/e94a402f-c6af-41e3-801a-34c8aa905c01)

### Unit Tests Executed

- src/test/java/programmingtheiot/part01/unit/common/ConfigUtilTest.java 
- src/test/java/programmingtheiot/part01/unit/common/ConfigUtilTest.java 
- src/test/java/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.java
- src/test/java/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.java


### Integration Tests Executed

- src/test/java/programmingtheiot/part01/integration/app/GatewayDeviceAppTest.java
- src/test/java/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.java

EOF.
