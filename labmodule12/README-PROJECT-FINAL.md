# Lab Module 12 - Semester Project - Final Write-up

NOTE: Be sure to implement all the Lab Module 12 requirements listed at [Lab Module 12](https://github.com/orgs/programming-the-iot/projects/1#column-10488565).


## Description

Introducing the Gas Storage Facility IoT Monitoring System project, a cutting-edge solution designed for the safety, operational efficiency, and environmental compliance of gas storage facilities. Through the integration of advanced sensors for pressure, temperature, and humidity, combined with a sophisticated monitoring platform, this system enables facility operators to automate safety protocols, closely monitor real-time environmental conditions, and effectively respond to potential hazards.



## What - The Problem 

In many households, conventional lighting systems lack flexibility and energy efficiency. People often forget to turn off lights when leaving a room, leading to unnecessary energy consumption. Additionally, manually adjusting lighting settings can be inconvenient. The proposed solution aims to address these issues by introducing an intelligent lighting system that automatically adapts to user behavior and preferences.

## Why - Who Cares? 

Energy conservation and user convenience are at the forefront of this project. By automating lighting control, users can significantly reduce energy waste and lower electricity bills. The system caters to individuals who want a more efficient and user-friendly approach to managing their home lighting. Furthermore, in an era where sustainability is a key concern, this system contributes to a greener and more energy-conscious lifestyle.



## How - Expected Technical Approach

In my gas storage facility IoT monitoring system, the Edge Tier architecture includes a pressure sensor, humidity sensor, and temperature sensor mounted on a constrained device. These sensors are critical for monitoring the safe and efficient operation of the gas storage facility. The temperature data is processed locally by the Cloud Data Analytics (CDA), which triggers the HVAC system or other relevant safety mechanisms when the temperature exceeds or falls below the set thresholds. All sensor readings are then transmitted to the Gateway Device Application (GDA) for further analysis and forwarding to the Cloud Tier.

Within the GDA, pressure readings are crucially analyzed. This involves comparing the received pressure data against established safety thresholds. If the pressure within the storage tanks falls below or exceeds these thresholds, it could indicate a leak or other hazardous situation, prompting the system to initiate emergency protocols, such as activating alarms or shutting down sections of the facility.

Humidity levels are also monitored to ensure that they remain within safe and optimal ranges, particularly in control rooms or areas where critical equipment is housed. Excessive humidity can lead to corrosion or equipment malfunction, while too low humidity might create an environment conducive to static electricity, a potential hazard in a gas storage facility.


### System Diagram

![MicrosoftTeams-image (1)](https://github.com/mondalso/piot-java-components/assets/124481330/dc99ab10-268e-4637-8672-c76dfadda903)

In the Edge Tier of my gas storage IoT monitoring system, the architecture diagram highlights the use of a pressure sensor, humidity sensor, and temperature sensor on a constrained device. These sensors are vital for ensuring the safety and efficiency of the gas storage facility. The temperature is continuously monitored by the Cloud Data Analytics (CDA), which triggers the HVAC system or other necessary safety mechanisms when it goes outside the safe range. The data from all these sensors are then sent to the gateway device for additional analysis and transmission to the Cloud Tier.

In the Gateway Device Application (GDA), the pressure data is critically analyzed. This process includes comparing the received pressure readings against a set safety range. If the pressure within the storage tanks drops below or exceeds this range, it could indicate a leak or a potential hazard, prompting the system to initiate emergency protocols such as activating alarms or shutting down sections of the facility.

Similarly, humidity levels within the facility are rigorously monitored. Should the humidity fall below or rise above the designated thresholds, it could signal conditions that might lead to equipment corrosion, gas condensation, or other safety risks. In such cases, the system could engage dehumidifiers or other control measures to maintain a stable and safe environment within the gas storage facility.

### What THREE (3) sensors and ONE (1) actuator did you use (add more if you wish)?

- CDA Sensor 1: Humidity Sensor 
- CDA Sensor 2: Temperature Sensor 
- CDA Sensor 3: Pressure Sensor 
- CDA Actuator 1: HVAC Actuator

### What ONE (1) CDA protocol and TWO (2) GDA protocols did you implement (add more if you wish)?

- CDA to GDA Protocol: MQTT over TLS
- GDA to CDA Protocol: MQTT over TLS
- GDA to Cloud Protocol: MQTT over TLS
- Cloud to GDA Protocol: MQTT over TLS

### What TWO (2) cloud services / capabilities did you use (add more if you wish)?

- Cloud Service 1 (data ingress - all inputs):
	- SensorData(Water Level Data, Temperature Data, Pressure Data)
	- SystemPerformanceData (CDA CPU Utilization, CDA Memory Utilization)
	- SystemPerformanceData (GDA CPU Utilization, GDA Memory Utilization)
- Cloud Service 2 (data egress - all actuation events):
	- Actuator Data (LED Actuator, HVAC Actuator)



## Screen Shots Representing Cloud Services
### Ubidots 

![image](https://github.com/mondalso/piot-java-components/assets/124481330/017fadb7-3381-4d0f-833e-3e74e60e4791)

### SenseHAT 

<img width="497" alt="image" src="https://github.com/mondalso/images/assets/124481330/c2724e7e-5548-4707-a783-007bdfded7d1">

### GDA Console 

<img width="751" alt="image" src="https://github.com/mondalso/images/assets/124481330/0caa59d3-b88e-4259-8804-ad6b4bbcf412">

### CDA Console 

<img width="905" alt="image" src="https://github.com/mondalso/images/assets/124481330/efefae64-72ec-4db0-ad00-2d4c10cd5d76">



EOF.
