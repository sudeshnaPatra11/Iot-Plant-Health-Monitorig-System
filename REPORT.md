# IoT Plant Monitoring System — Project Report

## 1. Project Information

**Course:** ECE4017 – IoT Domain Analyst  
**Project:** Plant Monitoring System  
**Type:** Group academic project

### Members
- 23BEC7083 — Saptadeepa Pal
- 23BEC7066 — Anurag Singh
- 23BEC7226 — Ruchika Sen
- 23BEC7264 — Sudeshna Patra

**Faculty:** Kritika Bansal

The supplied report presents a multi-parameter IoT plant monitoring architecture using distributed sensing, wireless communication, gateway processing, cloud analytics, dashboards and alerts. fileciteturn9file0L3-L16

## 2. Objectives

The report identifies these objectives:
1. Deploy a multi-parameter wireless sensor network.
2. Develop an edge gateway for aggregation and preprocessing.
3. Integrate cloud analytics, dashboards, alerting and ML predictions.
4. Provide information through web and mobile applications.
5. Quantify water-efficiency, yield and operational-cost improvements.
6. Create a scalable architecture. fileciteturn9file0L64-L70

## 3. Architecture

The system is described as four functional layers:

**Sensor Layer → Gateway Layer → Cloud Layer → Application Layer**

The sensor layer collects environmental parameters. A Raspberry Pi 4 gateway aggregates and preprocesses data. The cloud layer provides storage and analytics, while dashboards and notifications form the application layer. fileciteturn9file0L86-L124

## 4. Technical Design

The report specifies ATmega328P sensor nodes at 8 MHz, Zigbee IEEE 802.15.4 at 2.4 GHz, a 3.7 V 2000 mAh Li-ion battery and 5 V / 100 mA solar charging. The gateway is a Raspberry Pi 4 with Node-RED. The cloud stack is AWS IoT Core + InfluxDB v2, with Grafana 10 / React Native for visualization. fileciteturn9file0L170-L181

## 5. Data Flow

Sensor readings are collected every five minutes and transmitted by Zigbee. The gateway performs outlier detection and unit conversion before MQTT publishing. Cloud processing validates, aggregates and stores the readings; a rule engine evaluates threshold conditions and dispatches alerts. fileciteturn9file0L164-L181

## 6. Sensors

The documented sensor matrix includes:
- SEN-29SH — soil moisture
- SHT40-AD1B — temperature/humidity
- BH1750FVI — light
- SEN-0169 — soil pH
- SCD41 — CO2

fileciteturn9file0L209-L216

## 7. Machine Learning

The report states that the ML module predicted moisture-stress events with 91% accuracy up to four hours in advance. fileciteturn9file0L52-L56

The original model-training code is currently unavailable. This GitHub version therefore does not claim to reproduce the model or its accuracy. The ML result is retained as a project-reported result only.

## 8. Reported Deployment and Results

The report describes a pilot across three greenhouse facilities covering 4,800 m², with 16 managed zones, 48 sensor nodes and four gateway units. fileciteturn9file0L262-L267

Reported results include 27% lower water consumption, 22% higher tomato yield, 17.7% lower disease incidence, 76.7% lower manual inspection time, 99.2% sensor uptime and a 5.3% false-alert rate. fileciteturn9file0L321-L338

These values are reproduced from the supplied project report and are not independently verified by this repository.

## 9. Bill of Materials

The report lists ATmega328P, SHT40-AD1B, SEN-29SH, BH1750FVI, SCD41, XBee Series 2, Li-ion battery, solar panel, custom PCB, enclosure and miscellaneous hardware. The stated total is ₹4,060 per node. fileciteturn9file0L392-L411

## 10. Limitations of This GitHub Version

The following original source materials are currently unavailable:
- Sensor-node firmware
- Gateway software
- Cloud deployment/configuration
- Dashboard/mobile source
- ML training code

No unavailable implementation has been fabricated for this repository.

## 11. Future Scope

The supplied report proposes automated irrigation, expanded predictive analytics, LoRaWAN outdoor monitoring, fertiliser-management integration, ERP/market integration and carbon-footprint tracking. fileciteturn9file0L344-L350

## 12. Conclusion

The project demonstrates a layered IoT architecture for plant monitoring, connecting environmental sensing with wireless communication, edge processing, cloud analytics and user-facing alerts.

For portfolio purposes, this repository preserves the project's documented architecture and results while clearly separating available project documentation from source code that is currently missing.
