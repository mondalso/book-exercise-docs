# Constrained Device Application (Connected Devices)

## Lab Module 06


### Description

This implementation adds MQTT messaging capabilities to the Constrained Device Application (CDA) to enable publish/subscribe communication with other applications.The CDA can now connect to an MQTT broker, publish sensor data and status messages to specified topics, and subscribe to topics in order to receive incoming actuation commands. The Eclipse Paho MQTT Python client library is used to handle the MQTT protocol details.

Callbacks have been implemented to process connect/disconnect events and receive messages from subscribed topics. The MQTT client is initialized and connected/disconnected within the DeviceDataManager class.

When starting up, the CDA subscribes to an "Actuator Commands" topic in order to receive any actuation directives. The CDA can now publish sensor messages to separate sensor data and status topics periodically based on configuration.

This allows the CDA to integrate with other applications like the Gateway Device Application (GDA) using asynchronous, event-driven MQTT messaging. The publish/subscribe model facilitates flexible integration without direct dependencies between the applications.

### Code Repository and Branch

URL: https://github.com/mondalso/piot-python-components/tree/labmodule06

### UML Design Diagram(s)

This is the UML diagram depicting the classes added to the CDA workbench as part of labmodule06 and the relationship between each class.

![CDA-labmodule06](https://github.com/mondalso/images/blob/main/CDA-labmodule06.drawio.png)
[link to UML](https://github.com/mondalso/images/blob/main/CDA-labmodule06.drawio.png)

### Integration Tests Executed

- MqttClientConnectorTest


EOF.
