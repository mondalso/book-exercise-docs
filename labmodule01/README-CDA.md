# Constrained Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-01-001 - Lab Module 01](https://github.com/orgs/programming-the-iot/projects/1#column-9974937).

### Description

The initial enviroment setup for CDA dev environment was created by cloning the [python-components](https://github.com/programming-the-iot) repository. After cloning a copy of the repository locally, a remote git repository was created and linked using URL. 

The native operating system of the working system is Windows 11. Windows Susbsystem for Linus(WSL) was chosen as the installation approach. Once the WSL was in place, Eclipse was the IDE platform chosen for the lifecycle of the project and installed. The local repositories were imported to Eclipse and PyDev was installed. Neccessary paths were set and config was put in place to enable python runs. 

The first set of tests were to determine if the environment setup was working as expected. A new branch labmodule01 was created and part01 unit tests and integration tests were run. Once all tests passed, the branch was merged with the default branch main. 

### Code Repository and Branch
 
Repository - piot-python-components [https://github.com/mondalso/piot-python-components.git](https://github.com/mondalso/piot-python-components.git)
Branch - labmodule01 [https://github.com/mondalso/piot-python-components.git](https://github.com/mondalso/piot-python-components/tree/labmodule01)

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).


### Unit Tests Executed

- src/test/python/programmingtheiot/part01/unit/common/ConfigUtilTest.py

### Integration Tests Executed

- src/test/python/programmingtheiot/part01/integration/app/ConstrainedDeviceAppTest.py

EOF.
