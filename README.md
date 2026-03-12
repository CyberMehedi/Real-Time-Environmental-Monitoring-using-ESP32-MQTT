Real-Time Environmental Monitoring using ESP32 & MQTT

An IoT-based environmental monitoring system that collects real-time sensor data and transmits it to a cloud dashboard using the MQTT protocol. The system monitors temperature, humidity, and gas concentration to detect unsafe environmental conditions and provide real-time alerts.

This project demonstrates an end-to-end IoT pipeline integrating embedded systems, communication protocols, cloud platforms, and data visualization.

Project Overview

Poor indoor environmental conditions such as high temperature, humidity, and gas concentration can negatively impact health and safety. Traditional monitoring systems lack real-time visibility, remote access, and automated alerts.

This project solves that problem by using ESP32, MQTT communication, and the ThingsBoard cloud platform to provide continuous monitoring and real-time visualization.

System Architecture
Sensors → ESP32 → MQTT Broker → ThingsBoard Cloud → Dashboard → Alerts

Sensors collect environmental data

ESP32 processes the readings

Data is transmitted via MQTT protocol

Cloud platform visualizes the data

Alerts are triggered if thresholds are exceeded

Features

✔ Real-time environmental monitoring
✔ MQTT-based lightweight communication
✔ Cloud-based dashboard visualization
✔ Threshold-based safety detection
✔ OLED display for local monitoring
✔ LED alerts for unsafe conditions
✔ Secure MQTT authentication

Hardware Components
Component	Purpose
ESP32	Main microcontroller
DHT22	Temperature & humidity sensing
MQ Gas Sensor	Gas concentration detection
OLED Display	Local real-time data display
LED	Visual safety alert
Jumper Wires	Circuit connections
Software & Technologies

ESP32 (Embedded C / Arduino IDE)

MQTT Protocol

ThingsBoard Cloud Platform

IoT Dashboard Visualization

JSON Data Format

Example MQTT Message Format
{
  "temperature": 28,
  "humidity": 65,
  "gas": 1200
}

Topic:

v1/devices/me/telemetry
Safety Detection Logic
Gas > 3000        → UNSAFE
Temperature >40°C → WARNING
Humidity >70%     → WARNING
Else              → SAFE
Dashboard Visualization

The ThingsBoard dashboard displays:

Temperature time-series chart

Gas level gauge

Humidity numeric card

Safety status indicator

Security Considerations

Device authentication using access tokens

Secure MQTT communication

Restricted cloud access to authorized users

No personal data collection

Results

Real-time sensor data successfully transmitted

Cloud dashboard updates instantly

Gas threshold correctly triggers UNSAFE alerts

OLED and LED provide effective local feedback

Future Improvements

Mobile application integration

Email / SMS alert notifications

AI-based predictive analytics

Additional sensors (CO₂, PM2.5)

Edge-based anomaly detection

Contributors

Md Mehedi Hasan

Hasibullah Naeim

Anas Ismail Ahmed

License

This project is created for academic and educational purposes.
