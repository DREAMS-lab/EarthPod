# EarthPod-Datalogging
Environmental sensor datalogging for Raspberry Pi and Google Coral based sensor pods.

## Hardware

The code in this project is intended to be used in a sensor pod based on a Raspberry Pi or Google Coral. The primary sensing hardware is the Coral Environmental Sensor Board, which provides ambient light, barometric pressure, humidity, and temperature measurements. This board is compatible with both Google Coral and Raspberry Pi. Additional sensors can be connected to the Environmental Sensor Board through a series of Grove connectors.

## Programs

### enviro_logging.py

This program will create a .csv file that records the measurements captured by the sensors in the Environmental Sensor Board.

### enviro_logging_wind.py

This program adds functionality for reading wind speed using the sensor from a handheld anemometer.
