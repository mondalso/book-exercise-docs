# Gateway Device Application (Connected Devices)

## Lab Module 07

### Description

This implementation integrates the Eclipse Paho MQTT client library into the Gateway Device Application (GDA) to enable MQTT-based messaging between the GDA and other applications, such as the Constrained Device Application (CDA).

The GDA MQTT client is implemented in the MqttClientConnector class, which handles connecting to an MQTT broker, publishing messages, and subscribing to topics using the Eclipse Paho library. The MqttClientConnector is initialized based on configuration settings and its methods enable publishing messages and (un)subscribing to MQTT topics with specified QoS levels. It also implements callbacks to handle MQTT events like connection status changes, incoming messages, and delivery confirmations. The MqttClientConnector instance is created within the DeviceDataManager, which handles (un)subscribing from relevant MQTT topics when starting/stopping to receive messages published from other applications.

### Code Repository and Branch


URL: https://github.com/mondalso/piot-java-components/tree/labmodule07

### UML Design Diagram(s)

This is the UML diagram depicting the classes added to the CDA workbench as part of labmodule07 and the relationship between each class.
![CDA-labmodule07](https://github.com/mondalso/images/blob/main/GDA-labmodule07.drawio.png)
[link to UML](https://github.com/mondalso/images/blob/main/GDA-labmodule07.drawio.png)

### Integration Tests Executed

- MqttClientConnectorTest


EOF.
