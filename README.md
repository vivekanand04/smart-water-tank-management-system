# 💧 IoT Water Tank Monitoring System with Mobile App Integration 📱

Monitor your water tank levels remotely with our IoT-based system. Get real-time updates on your mobile device via our dedicated app.



## 📝 Overview

This project demonstrates interfacing water level sensors with an ESP8266 (D1 R1) and controlling LEDs through Wi-Fi using the Blynk app. The LEDs indicate the water level, and the project includes integration with a water level depth detection sensor for precise readings.

## ✨ Features

* **Real-time Monitoring**: Continuously monitor water levels in your tank.
* **Mobile App Integration**: Receive updates and control the system via the Blynk mobile app.
* **LED Indicators**: Visual representation of water levels using LEDs.
* **Connectivity Status**: Monitor network connectivity through an additional LED indicator.

## 🔧 Hardware Components

* **Wemos ESP8266 Wi-Fi Board (D1 R1)**

  * Microcontroller: ESP8266 (D1 R1)
  * Clock Speed: 80MHz (up to 160MHz)
  * USB Converter: CH340G
  * Operating Voltage: 3.3V
  * Flash Memory: 4MB
  * Digital I/O: 11
  * Analog Inputs: 1
  * Communications: I2C, Serial, SPI
  * WiFi: Built-in

* **LEDs**: 3.3V LEDs (Red, Green, Blue, Yellow)

* **Water Level Depth Detection Sensor**

  * Operating Voltage: DC 3-5V
  * Operating Current: < 20mA
  * Sensor Type: Analog
  * Detection Area: 40mm x 16mm
  * Operating Temperature: 10°C-30°C
  * Humidity: 10% - 90% non-condensing

* **Jumper Wires**: Female, Male to Male

* **Breadboard**: Full-size Breadboard

## 🔌 Circuit Diagram

```
                               _____________________
                              |          |          |
                              |    D2    |    D3    |
                              |__________|__________|
                              |          |          |
                              |    D6    |    D10   |
                              |__________|__________|            ____________
                              |          |          |           |            |
                              |    D1    |    GND   |---------- |  ESP8266   |
                              |__________|__________|  |        |____________|
                              |          |          |  |
                              |    A0    |   3.3v   |  |
                              |__________|__________|  |
                                  |          |         |
                                  |          |         |
                                  |          |         |         ____________
                                  |          |         |        |            |
                                  |__________|_________|________|   Sensor   |
                                                                |____________|
```

* **D2, D3, D6, D10**: Pins connected to LEDs.
* **D1**: Pin used to indicate connectivity.
* **A0**: Analog pin connected to the water level depth detection sensor.
* **GND**: Ground connection.
* **ESP8266**: Wemos ESP8266 Wi-Fi Board (D1 R1)
* **Sensor**: Water Level Depth Detection Sensor

## 🛠️ Setup Instructions

### 1. Circuit Connection

1. **Connect LEDs**:

   * Connect LEDs (3.3V Red, Green, Blue, Yellow LEDs) to pins D2, D3, D6, and D10 on the ESP8266 board.
   * Connect the negative (shorter) lead of each LED to the ground (GND) on the breadboard to complete the circuit.

2. **Connectivity Indicator**:

   * Connect pin D1 to indicate network and cloud connectivity.

3. **Sensor Connection**:

   * Connect the water level depth detection sensor to pin A0, GND, and 3.3V on the ESP8266 board.

### 2. Blynk App Configuration

1. **Web Interface Setup**:

   * Go to the Blynk website and sign up for an account.
   * Once logged in, create a new project and select the ESP8266 board.
   * Configure the project settings and choose the appropriate connection type (Wi-Fi).
   * Add widgets to the project dashboard to control the LEDs and monitor connectivity.

2. **Variable Setup**:

   * Create virtual pins in your Blynk project to communicate with the ESP8266.
   * Assign each LED and connectivity indicator to a specific virtual pin.

### 3. Arduino Code Configuration

1. **Open the Arduino Code**:

   * Open the Arduino code file `Water_Tank_Monitoring_System.ino` from this repository.

2. **Configure the Code**:

   * Include the Blynk library and configure the Wi-Fi credentials.
   * Initialize Blynk with your authentication token and connect to the Blynk server.
   * Map the virtual pins to the corresponding LEDs and connectivity indicators.
   * Implement functions to handle LED control, monitor connectivity status, and read data from the water level depth detection sensor.

### 4. Running the Project

1. **Power the ESP8266**:

   * Connect your ESP8266 board to power and ensure it is connected to the Wi-Fi network.

2. **Use the Blynk App**:

   * Open the Blynk app on your mobile device and navigate to the project dashboard.
   * Use the widgets to control the LEDs, monitor connectivity, and view water level readings.
   * Test different scenarios and functionalities to ensure proper operation.

## 📸 Screenshots

*Include relevant screenshots here to showcase the mobile app interface and system setup.*

## 📝 License

This project is licensed under the MIT License. Feel free to use, modify, and distribute this project for educational purposes.

*Disclaimer: This project is intended for educational purposes only and should not be used in production environments without proper testing and validation.*
