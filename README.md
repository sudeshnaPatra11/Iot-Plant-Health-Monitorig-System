# IoT Plant Monitoring System

### IoT-based multi-parameter monitoring and analytics platform for precision agriculture

**Group project — VIT-AP, ECE4017 (IoT Domain Analyst)**

## Overview

This project explores an IoT-based plant monitoring architecture for greenhouse/precision-agriculture environments. The supplied project report describes distributed sensor nodes, an IoT gateway, cloud storage and analytics, dashboards, threshold-based alerts, and a machine-learning component for moisture-stress prediction.

The documented system monitors:
- Soil moisture
- Temperature
- Relative humidity
- Light intensity
- Soil pH
- CO2 concentration

The report specifies ATmega328P sensor nodes, Zigbee communication, a Raspberry Pi 4 gateway, AWS IoT Core + InfluxDB, and Grafana/React Native visualization. See the architecture on pages 5–6 of the supplied report. fileciteturn9file0L86-L126

## System Architecture

```text
Sensor Layer
  Soil moisture | Temperature | Humidity | Light | pH | CO2
                         |
                       Zigbee
                         |
                         v
Gateway Layer
  Raspberry Pi 4
  Aggregation + preprocessing + MQTT
                         |
                         v
Cloud Layer
  AWS IoT Core + InfluxDB
  Analytics + ML
                         |
                         v
Application Layer
  Grafana / Mobile App / Alerts / Reports
```

The report describes sensor readings being collected every five minutes, transmitted via Zigbee, preprocessed at the gateway, published through MQTT, and then validated, aggregated and stored in the cloud. fileciteturn9file0L164-L181

## Sensor Node

According to the report, each sensor node uses an ATmega328P at 8 MHz, Zigbee IEEE 802.15.4 at 2.4 GHz, a 3.7 V 2000 mAh Li-ion battery and a 5 V / 100 mA solar panel. fileciteturn9file0L125-L129

The documented sensor set is:

| Parameter | Sensor |
|---|---|
| Soil moisture | SEN-29SH |
| Air temperature | SHT40-AD1B |
| Relative humidity | SHT40-AD1B |
| Light | BH1750FVI |
| Soil pH | SEN-0169 |
| CO2 | SCD41 |

fileciteturn9file0L209-L216

## Alert System

The documented workflow is:

```text
Threshold exceeded
      ↓
Rule engine
      ↓
Alert triggered
      ↓
SMS / Email / Push / Dashboard
      ↓
Action logged
```

fileciteturn9file0L223-L230

Default thresholds in the report include soil moisture 35–75% VWC warning range, temperature 15–32 °C, humidity 50–85% RH, pH 5.8–7.2, and CO2 400–1200 ppm. fileciteturn9file0L231-L243

## Machine Learning

The project report states that an integrated ML module predicted moisture-stress events with 91% accuracy up to four hours in advance. fileciteturn9file0L52-L56

**Important:** the original model-training code is currently unavailable. This repository therefore does **not** invent or recreate the training implementation, and the 91% figure is documented as a **reported project result**, not as an independently reproduced result.

The `ml/` folder is reserved for the original training code when it becomes available.

## Reported Pilot Results

The supplied report gives these results:

| KPI | Baseline | Post-deployment | Reported change |
|---|---:|---:|---:|
| Water consumption | 2,840 L/week | 2,074 L/week | −27.0% |
| Tomato yield | 18.2 t/ha | 22.2 t/ha | +22.0% |
| Disease incidence | 12.4/month | 10.2/month | −17.7% |
| Manual inspection | 120 hrs/month | 28 hrs/month | −76.7% |
| Alert response | N/A | <90 s | — |
| Sensor uptime | N/A | 99.2% | — |
| False alert rate | N/A | 5.3% | — |

These are **figures reported in the supplied group report**; this GitHub repository does not claim independent reproduction. fileciteturn9file0L321-L338

## Group Project

The supplied report lists:
- Saptadeepa Pal
- Anurag Singh
- Ruchika Sen
- Sudeshna Patra

Faculty: Kritika Bansal. fileciteturn9file0L11-L16

### My Contribution

Add your exact individual contribution here. Do not imply that you personally developed every part of the group project.

Suggested categories, **only if accurate**:
- Hardware / sensor integration
- Data acquisition
- IoT architecture
- Sensor testing
- Data preprocessing
- Model-training support
- Documentation / presentation

## Current Repository Scope

The original source code for the sensor firmware, gateway, cloud deployment, dashboard/mobile application and ML training is not currently available. This repository therefore documents the project architecture, report and reported results rather than pretending to contain unavailable implementation code.

## Future Work

The supplied report recommends:
- Automated irrigation actuation
- Expanded predictive analytics
- LoRaWAN outdoor monitoring
- Fertiliser-management integration
- ERP/market integration
- Carbon-footprint tracking

fileciteturn9file0L340-L350

## Technologies

IoT • Embedded Systems • ATmega328P • Zigbee • Raspberry Pi • MQTT • AWS IoT Core • InfluxDB • Grafana • React Native • Machine Learning • Precision Agriculture

## Repository Structure

```text
IoT-Plant-Monitoring-System/
├── README.md
├── REPORT.md
├── docs/
│   └── architecture-notes.md
├── ml/
│   └── README.md
└── figures/
    └── README.md
```
