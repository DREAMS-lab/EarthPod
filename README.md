# EarthPod
Code for the [EarthPod](https://twitter.com/ASU_GDCS/status/1277711451856211975) environmental sensor pod.


## Datalogging-Arduino

### Hardware

The code in this folder is intended to be used in a sensor pod based on a Adafruit Feather M0 Adalogger. Connected sensors include:

- DS3231 RTC
- FXAS21002C Gyroscope
- FXOS8700 Acclerometer/Magnetometer
- BME280 Air Pressure/Temperature/Humidity Sensor
- TCS34725 Color Sensor (for determining wind direction)
- SI1145 Light/UV Index Sensor

### feather-all-i2c.ino

This program will initialize all sensors and print readings to the serial terminal

### feather-all-i2c-logging-2.ino

This program will create a .csv file on the Adalogger's SD card that records the measurements captured by the sensors. Some sections are currently commented out so that the program can be tested on an Adafruit Feather 32u4 Adalogger.

### feather-anemometer.ino

Test initialization and interrupts for a wind speed sensor from a [handheld anemometer](https://www.amazon.com/Anemometer-Velocity-Measurement-Thermometer-Windsurfing/dp/B01JOTJMU6/).


## Datalogging-Python

### Hardware

The code in this folder is intended to be used in a sensor pod based on a Raspberry Pi or Google Coral. The primary
sensing hardware is the Coral Environmental Sensor Board, which provides ambient light, barometric pressure, humidity, and temperature measurements. This board is compatible with both the Google Coral and Raspberry Pi. Additional sensors can be connected to the Environmental Sensor Board through a series of Grove connectors.

### enviro\_logging.py

This program will create a .csv file that records the measurements captured by the sensors in the Environmental Sensor
Board.

### enviro\_logging\_wind.py

This program adds functionality for reading wind speed using the sensor from a [handheld anemometer](https://www.amazon.com/Anemometer-Velocity-Measurement-Thermometer-Windsurfing/dp/B01JOTJMU6/).

### enviro\_logging\_wind\_airflow.py

This program adds functionality for reading wind speed using a [F662 Board Mount Airflow Sensor](https://www.degreec.com/pages/f660-662) from Degree Controls.


## MagnetRelease

### MagnetRelease.ino

Arduino program for the twist-release magnet system used to deploy the pod.
