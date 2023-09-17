# Gateway Device Application (Connected Devices)

## Lab Module 01

### Description

The initial enviroment setup for GDA dev environment was created by cloning the [java-components](https://github.com/programming-the-iot/java-components) repository. After cloning a copy of the repository locally, a remote git repository was created and linked using URL.

The native operating system of the working system is Windows 11. Windows Susbsystem for Linus(WSL) was chosen as the installation approach. Once the WSL was in place, Eclipse was the IDE platform chosen for the lifecycle of the project and installed. The local repositories were imported to Eclipse and Maven was installed to enable java runs from command line.

The first set of tests were to determine if the environment setup was working as expected. A new branch labmodule01 was created and part01 unit tests and integration tests were run. Once all tests passed, the branch was merged with the default branch main.

### Code Repository and Branch

Repository - [piot-java-components](https://github.com/mondalso/piot-java-components.git)

Branch - [labmodule01](https://github.com/mondalso/piot-java-components/tree/labmodule01)


### UML Design Diagram(s)

labmodule01 was about environment setup and there was no coding involved. Hence, there is no UML diagram included.

### Unit Tests Executed

- src/test/java/programmingtheiot/part01/unit/common/ConfigUtilTest.java 

### Integration Tests Executed

- src/test/java/programmingtheiot/part01/integration/app/GatewayDeviceAppTest.java

EOF.
