# Architecture Notes

Sensor Layer → Gateway Layer → Cloud Layer → Application Layer

- Sensor layer: ATmega328P nodes measuring soil moisture, temperature, humidity, light, pH and CO2.
- Gateway: Raspberry Pi 4 for aggregation and preprocessing.
- Communication: Zigbee between sensor nodes and gateway; MQTT for cloud publishing.
- Cloud: AWS IoT Core + InfluxDB.
- Application: Grafana dashboard and React Native mobile application.
- Alerts: SMS, email, push notification and dashboard banner.

The project report specifies a five-minute sensor sampling interval.
