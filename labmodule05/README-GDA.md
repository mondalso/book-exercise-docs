# Gateway Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-05-001 - Lab Module 05](https://github.com/orgs/programming-the-iot/projects/1#column-10488421).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

### Code Repository and Branch

Repository - [piot-java-components](https://github.com/mondalso/piot-java-components.git)

Branch - [labmodule05](https://github.com/mondalso/piot-java-components/tree/labmodule05)

### UML Design Diagram(s)

This is the UML diagram depicting the classes added to the GDA workbench as part of labmodule02 and the relationship between each class.
![GDA-labmodule05](https://github.com/mondalso/images/blob/main/GDA-labmodule05.jpg)
[link to UML](https://github.com/mondalso/images/blob/main/GDA-labmodule05.jpg)

### Unit Tests Executed

From Previous:

- src/test/java/programmingtheiot/part01/unit/common/ConfigUtilTest.java 
- src/test/java/programmingtheiot/part01/unit/common/ConfigUtilTest.java 
- src/test/java/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.java
- src/test/java/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.java

New:

- src/test/java/programmingtheiot/part02/unit/data/ActuatorDataTest.java
- src/test/java/programmingtheiot/part02/unit/data/SensorDataTest.java
- src/test/java/programmingtheiot/part02/unit/data/SystemPerformanceDataTest.java
- src/test/java/programmingtheiot/part02/unit/data/SystemStateDataTest.java
- src/test/java/programmingtheiot/part02/unit/data/DataUtilTest.java

### Integration Tests Executed

From previous:

- src/test/java/programmingtheiot/part01/integration/app/GatewayDeviceAppTest.java
- src/test/java/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.java

New:

- src/test/java/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.java
- src/test/java/programmingtheiot/part02/integration/data/DataIntegrationTest.java
- src/test/java/programmingtheiot/part02/integration/app/DeviceDataManagerNoCommsTest.java
- src/test/java/programmingtheiot/part01/integration/app/GatewayDeviceAppTest.java

EOF.
