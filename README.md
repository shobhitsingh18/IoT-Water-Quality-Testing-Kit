# IoT Based Bacteriological Water Contamination Testing Kit

## Overview
This project is a prototype for a portable, digital testing kit designed to detect bacteriological contamination in water. The system is built using ESP32 microcontrollers, Raspberry Pi, and various sensors to measure water quality parameters. A machine learning model is implemented to estimate the percentage of colony-forming units (CFU) in contaminated water samples.

## Features
- **Multi-Sensor Integration**: Measures parameters including pH, turbidity, TDS, temperature, and optical properties.
- **Dual ESP32 System**: One ESP32 is dedicated to optical sensors, while the other handles pH, turbidity, temperature, and TDS sensors.
- **Real-Time Data Processing**: Sensor data is processed and displayed digitally.
- **ML-Based Prediction**: A machine learning model on a Raspberry Pi predicts the percentage of bacterial contamination.
- **Battery-Powered**: Designed for portability with a rechargeable battery.
- **User-Friendly Interface**: OLED display for direct readings and optional cloud-based monitoring.

## Hardware Components
1. **ESP32 (x2)** - One for optical sensors, one for other water quality sensors.
2. **Raspberry Pi 4 Model B** - Runs the ML model to predict contamination levels.
3. **Sensors**:
   - **TCS3200 & TCS34725**: Optical sensors for color-based bacterial detection.
   - **pH Sensor**: Measures acidity levels.
   - **Turbidity Sensor**: Determines water clarity.
   - **TDS Meter V1.0**: Checks total dissolved solids.
   - **DS18B20 Temperature Sensor**: Measures water temperature.
4. **1.3” I2C OLED Display** - Displays real-time sensor readings.
5. **3000mAh Battery & Step-Up Converter** - Ensures reliable power supply.

## Software Implementation
- **Sensor Data Acquisition**: ESP32 microcontrollers read and transmit data.
- **Machine Learning Algorithm**: A trained model runs on the Raspberry Pi to predict contamination levels.
- **Data Visualization**: Results are displayed on the OLED screen and can be uploaded to Adafruit IO for cloud monitoring.
- **Self-Calibration Protocol**: Ensures accuracy by periodically calibrating sensor readings.

## Data Collection & Model Training
A dataset was developed including:
- pH
- TDS
- Turbidity
- RGB values from **TCS3200** and **TCS34725** sensors
The ML model was trained using historical water contamination data and validated against lab-tested samples.

## Future Improvements
- Integration with a mobile app for remote monitoring.
- Enhanced ML model for more precise bacterial detection.
- Improved power efficiency for extended operation.

## Repository Structure
```
/ ├── code/  # ESP32 and Raspberry Pi scripts
   ├── data/  # Collected datasets
   ├── images/  # Infographs
   ├── hardware/  # Circuit schematics and component details
   ├── README.md  # Project overview
```

## How to Use
1. Power on the device.
2. Insert the water sample into the testing module.
3. Wait for sensor data to be collected.
4. View results on the OLED display.
5. (Optional) Upload data to the cloud for further analysis.



For inquiries, contact singhshobhit2020@gmail.com

