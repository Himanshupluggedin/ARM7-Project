# IoT-Based Temperature and Humidity Monitoring using LPC2148 and ESP8266

This project measures temperature and humidity using a DHT11 sensor and uploads the data to ThingSpeak IoT Cloud via the ESP8266 Wi-Fi module. It is implemented on the LPC2148 ARM7 microcontroller in Embedded C.

---

## Overview

The system reads real-time temperature and humidity from the DHT11 sensor, processes the data using LPC2148, and transmits it to the ThingSpeak server using an ESP8266 module through UART communication. The readings can be monitored on the ThingSpeak dashboard.

---

## Hardware Requirements

- LPC2148 ARM7 Microcontroller  
- DHT11 Temperature and Humidity Sensor  
- ESP8266 Wi-Fi Module  
- USB-to-UART Converter (for serial monitoring)  
- 3.3V Power Supply  
- Jumper Wires and Breadboard  

---

## Software Requirements

- Keil µVision or VS Code (ARM GCC)  
- Flash Magic (for programming LPC2148)  
- ThingSpeak Account  
- Serial Terminal Software (PuTTY / TeraTerm)

---

## System Description

1. The DHT11 sensor provides humidity and temperature data through GPIO pin P1.16.  
2. LPC2148 reads this data, converts it into ASCII format, and sends it via UART to ESP8266.  
3. ESP8266 connects to Wi-Fi and transmits the data to ThingSpeak using HTTP GET requests.  
4. ThingSpeak displays the data in graphical format in the user’s channel.

---

## Pin Configuration

| Module | LPC2148 Pin | Description |
|---------|--------------|-------------|
| DHT11 Data | P1.16 | Sensor data input |
| ESP8266 TX | P0.1 | UART0 RX |
| ESP8266 RX | P0.0 | UART0 TX |
| Power | 3.3V | Shared supply |
| Ground | GND | Common ground |

---


