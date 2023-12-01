# Gateway Device Application (Connected Devices)

## Lab Module 08

### Description


This implementation integrates a CoAP server into the Gateway Device Application (GDA) using the Eclipse Californium library. It allows the Constrained Device Application (CDA) to send sensor data to the GDA and retrieve actuator commands using CoAP request/response messaging.

The CoAP server functionality is handled by the CoapServerGateway class, which provides an adapter to the Eclipse Californium library's CoapServer. The server manages CoAP resources and routes requests to specific resource handlers that process and respond to GET and PUT requests. Custom resource handlers were implemented to receive sensor data and system performance data from the CDA via PUT requests. Another handler allows the CDA to retrieve pending actuator commands via GET requests and supports observer notifications using CoAP. These CoAP resource handlers interface with the GDA's DeviceDataManager to process data and actuator messages. Overall, this enables CoAP-based integration between the CDA and GDA for sending telemetry and receiving actuator commands.


### Code Repository and Branch

URL: https://github.com/mondalso/piot-java-components/tree/labmodule08

### UML Design Diagram(s)

This is the UML diagram depicting the classes added to the CDA workbench as part of labmodule08 and the relationship between each class.
![GDA-labmodule08](https://github.com/mondalso/images/blob/main/GDA-labmodule08.drawio.png)
[link to UML](https://github.com/mondalso/images/blob/main/GDA-labmodule08.drawio.png)

### Integration Tests Executed

- CoapServerGatewayTest

EOF.
