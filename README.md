# 🌊 Early Detection of Flash Flood and Landslide using IoT and Machine Learning

A real-time early warning system that uses IoT sensor networks and machine learning to predict flash floods and landslides in high-risk mountainous regions. This project aims to save lives and reduce property damage by issuing timely alerts and enabling informed evacuation decisions.

---

## 📖 Table of Contents

- [Overview](#-overview)
- [System Architecture](#-system-architecture)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Hardware Components](#-hardware-components)
- [Machine Learning Models](#-machine-learning-models)
- [Folder Structure](#-folder-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Limitations](#-limitations)
- [Future Enhancements](#-future-enhancements)
- [Team](#-team)
- [License](#-license)

---

## 🧭 Overview

Flash floods and landslides are sudden and destructive natural disasters, especially prevalent in mountainous terrains such as the Himalayas. Traditional systems fail to provide timely alerts due to lack of real-time data and predictive capability.

This project integrates:
- **IoT-based sensor networks** for environmental monitoring
- **Machine learning models** for real-time prediction
- **Alert mechanisms** (SMS, buzzer, LED indicators) for emergency communication

---

## 🏗️ System Architecture

![System Architecture](images/system_architecture.png)


---

## 🌟 Key Features

- Real-time environmental monitoring
- Flash flood and landslide prediction using ML
- Offline alert triggering with buzzer and LEDs
- SMS alerts via Twilio or GSM module
- Dashboard for real-time visualization and control
- Modular and scalable system architecture

---

## 🧰 Tech Stack

| Component        | Tools Used                                        |
|------------------|---------------------------------------------------|
| Hardware         | ESP32, Arduino, Rain Sensor, Soil Moisture, IMU  |
| Programming      | Python, C++, Arduino IDE                         |
| Machine Learning | Scikit-learn (Random Forest, KNN, Logistic Regression) |
| Cloud/Storage    | Firebase / Google Cloud / Local server           |
| Frontend         | HTML/CSS/JS or React (Optional)                  |
| Alerting         | Twilio API, GSM module, LED, Buzzers             |

---

## 🔩 Hardware Components

| Component               | Purpose                                        |
|-------------------------|------------------------------------------------|
| Soil Moisture Sensor    | Monitor soil saturation to detect landslides   |
| Water Level Sensor      | Detect sudden water level rise (floods)        |
| Rainfall Sensor         | Measure rainfall intensity                     |
| Vibration Sensor        | Detect tremors and slope movements             |
| IMU / Tilt Sensor       | Measure slope angle changes                    |
| ESP32/Arduino           | Data collection and transmission               |
| GSM/LoRa Module         | Remote data communication                      |
| Battery + Solar Panel   | Power in remote areas                          |

---

## 🧠 Machine Learning Models

| Model              | Role                                                |
|--------------------|-----------------------------------------------------|
| Logistic Regression| Basic classification (Safe vs. Danger)             |
| K-Nearest Neighbors| Pattern-based prediction from historical data       |
| Random Forest      | Final classifier with high accuracy and robustness |

### 🔢 Input Features

- Rainfall (current and 24-hour)
- Soil moisture %
- Water level rise (cm/hr)
- Vibration intensity
- Slope angle
- Time of day / seasonality

### 🧪 Evaluation Metrics

- Accuracy, Precision, Recall, F1-Score
- Confusion Matrix
- Feature Importance (from Random Forest)

---


## 📁 Folder Structure


---

## 🚀 Usage

1. **Deploy and power the sensor nodes**  
   - Connect rainfall, soil moisture, vibration, and water level sensors to your ESP32/Arduino board.  
   - Ensure power is supplied via battery or solar panel in field conditions.

2. **Data Transmission**  
   - Sensor readings are collected by the microcontroller.
   - Data is sent to the local server or cloud (depending on connectivity).

3. **Real-Time ML Prediction**  
   - The `run_inference.py` script continuously analyzes incoming data using trained machine learning models.
   - Each data point is classified into one of three risk categories:  
     - `0`: Safe  
     - `1`: Warning  
     - `2`: Critical  

4. **Risk-Based Alerting**  
   - If risk level is `Warning` or `Critical`:
     - 🚨 Buzzer and LEDs are activated for immediate local notification.
     

---

