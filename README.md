# digital-twin-portfolio
# M1: IIoT Sensor Dashboard

## What It Does
Simulates a CNC machine publishing real-time sensor data (temperature, vibration, spindle speed)
via MQTT, stores it in InfluxDB, and visualizes it live on a Grafana dashboard.

## Architecture
Python Publisher → MQTT (Mosquitto) → Python Subscriber → InfluxDB → Grafana

## Tech Stack
- Python 3.12, paho-mqtt, influxdb-client
- MQTT Broker: Eclipse Mosquitto
- Database: InfluxDB v2
- Dashboard: Grafana

## How to Run
1. Start Mosquitto: `mosquitto -v`
2. Start subscriber: `python M1_sensor_subscriber.py`
3. Start publisher: `python M1_sensor_publisher.py`
4. Open Grafana: http://localhost:3000
