# Smart-Irrigation-System-Arduino
Arduino-based smart irrigation system that automatically waters plants based on soil moisture.

🌱 Smart Irrigation System using Arduino

An Arduino-based Smart Irrigation System that automatically waters plants when the soil becomes dry.

The system uses a soil moisture sensor to continuously monitor the moisture level of the soil. When the moisture level falls below a predefined threshold, Arduino activates a water pump through a relay and automatically irrigates the plant.

🌐 Live Project Website

"Smart Irrigation System" (https://smartirrigation01.netlify.app/)

The website contains the complete project information, circuit connections, working principle, Arduino code and calibration procedure.

---

📌 About the Project

Traditional watering methods require regular manual monitoring and may result in overwatering or underwatering.

This project provides an automatic solution. A soil moisture sensor measures the moisture level of the soil and sends the reading to an Arduino Uno.

Arduino compares the moisture level with a predefined threshold.

- If the soil is sufficiently moist → Pump remains OFF.
- If the soil becomes dry → Pump turns ON.
- After the watering cycle → Pump turns OFF.

This helps reduce unnecessary water usage and makes plant watering more convenient.

---

🎯 Objectives

- Automatically detect soil moisture.
- Water plants only when required.
- Reduce unnecessary water usage.
- Remove the need for regular manual watering.
- Learn Arduino-based automation.
- Build a simple and affordable smart agriculture project.

---

⚙️ Features

- 🌱 Automatic plant watering
- 💧 Soil moisture monitoring
- 🤖 Arduino-based automation
- 🔌 Relay-controlled water pump
- 📊 Moisture percentage calculation
- ⏱️ Automatic watering cycle
- 🖥️ Optional LCD display
- 💰 Low-cost implementation
- 🔧 Adjustable moisture threshold

---

🧰 Components Required

Component| Quantity
Arduino Uno/Nano| 1
Capacitive Soil Moisture Sensor| 1
5V Single-Channel Relay Module| 1
Mini Submersible Water Pump| 1
External Power Supply| 1
Silicone Water Tube| ~1 m
Breadboard| 1
Jumper Wires| As required
16×2 I2C LCD| Optional
DHT11 Sensor| Optional

---

🔌 Circuit Connections

Soil Moisture Sensor

Sensor Pin| Arduino
VCC| 5V
GND| GND
AOUT| A0

Relay Module

Relay Pin| Arduino
VCC| 5V
GND| GND
IN| D7

Optional I2C LCD

LCD Pin| Arduino
SDA| A4
SCL| A5

The water pump should use a suitable external power supply and be switched through the relay.

«⚠️ Important: Do not power the water pump directly from the Arduino 5V pin. The pump can draw more current than the Arduino can safely provide.»

---

🧠 How the System Works

1. Soil Moisture Detection

The capacitive soil moisture sensor continuously measures the moisture level of the soil.

2. Arduino Reads the Sensor

The sensor provides an analog value to Arduino through pin A0.

3. Moisture Calculation

Arduino converts the raw sensor reading into an approximate moisture percentage using calibrated dry and wet values.

4. Threshold Comparison

The moisture percentage is compared with the predefined threshold.

The default threshold used in this project is:

35%

5. Pump Activation

If the soil moisture falls below the threshold, Arduino activates the relay.

The relay switches ON the water pump.

6. Automatic Watering

The pump runs for a predefined amount of time and then turns OFF.

7. Continuous Monitoring

Arduino continues checking the soil at regular intervals.

---

💻 Arduino Code

The complete Arduino code is available in:

Arduino_Code/smart_irrigation.ino

The main settings include:

const int SOIL_SENSOR_PIN = A0;
const int RELAY_PIN = 7;

const int MOISTURE_THRESHOLD = 35;

const unsigned long PUMP_RUN_TIME = 5000;

const unsigned long CHECK_INTERVAL = 60000;

You can change these values according to your soil, sensor and pump.

---

🚀 How to Run the Project

Step 1

Download or clone this repository.

Step 2

Open:

Arduino_Code/smart_irrigation.ino

using the Arduino IDE.

Step 3

Connect the components according to the circuit diagram.

Step 4

Connect the Arduino to your computer.

Step 5

Select the correct:

- Board
- COM Port

Step 6

Upload the program to Arduino.

Step 7

Place the soil moisture sensor into the soil.

Step 8

Power the pump using a suitable external power supply.

Step 9

Test the system by changing the moisture level of the soil.

---

🔧 Sensor Calibration

Different soil moisture sensors can give different readings, so calibration is important.

Dry Value

1. Keep the sensor dry.
2. Read the analog value from A0.
3. Record the stable reading.
4. Use this value as "DRY_VALUE".

Wet Value

1. Put the sensor into wet soil or water as appropriate for your sensor.
2. Record the stable reading.
3. Use this value as "WET_VALUE".

Example:

const int DRY_VALUE = 620;
const int WET_VALUE = 310;

These values should be adjusted according to your actual sensor.

---

📸 Project Images

Add your actual project photographs here.

Complete Project

"Smart Irrigation System" (Images/project.jpg)

Circuit

"Circuit Diagram" (Images/circuit.jpg)

Working Model

"Working Model" (Images/working.jpg)

---

🌐 Live Website

Visit the complete project documentation:

https://smartirrigation01.netlify.app/

---

🔮 Future Improvements

Possible future improvements include:

- 📱 Mobile application for monitoring
- 🌐 IoT-based remote monitoring
- ☁️ Cloud data storage
- 🌧️ Rain sensor integration
- 🌡️ DHT11/DHT22 temperature and humidity monitoring
- 📊 Online moisture graphs
- 🔘 Manual pump control
- 🌱 Multiple irrigation zones
- 📡 ESP8266/ESP32-based wireless control
- 🔔 Mobile notifications

---

🛠️ Technologies Used

- Arduino
- C/C++
- Soil Moisture Sensor
- Relay Module
- Water Pump
- HTML
- CSS
- JavaScript

---

📂 Project Structure

Smart-Irrigation-System-Arduino/
│
├── README.md
│
├── Arduino_Code/
│   └── smart_irrigation.ino
│
├── Circuit_Diagram/
│   └── circuit_diagram.png
│
├── Images/
│   ├── project.jpg
│   ├── circuit.jpg
│   └── working.jpg
│
└── LICENSE

---

👨‍💻 Author

Adarsh Kumar Sah

Student
Academy of Technology

Skills

- C/C++
- Arduino
- HTML
- CSS
- JavaScript

---

⭐ Project Status

Completed — Working Prototype

This project was developed as an educational Arduino-based smart agriculture and automation project.

If you found this project useful, consider giving the repository a ⭐.
