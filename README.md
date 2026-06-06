# Smart Watering Automation using Artificial Neural Network

This repository contains a prototype implementation for a smart agricultural/IoT automation system. It builds and trains a binary classifier using an Artificial Neural Network (ANN) to predict whether a crop requires watering based on real-time environmental telemetry data.

By processing complex interactions between soil moisture, heat, and sun exposure, the deep learning model aims to replace traditional rigid threshold-based irrigation with intelligent, resource-efficient watering schedules.



## 🧠 Telemetry Features & Data Model
The network learns from a multidimensional feature matrix to predict a binary state (`needs_water`):

* **Soil Moisture:** Volumetric water content ratio (scaled 0.0 to 1.0).
* **Temperature:** Ambient heat reading in Celsius (°C).
* **Sunlight Hours:** Total hours of continuous sun exposure.
* **Target (`needs_water`):** Binary output where `1` indicates immediate watering is required and `0` indicates no action needed.

## 🏗️ Neural Network Architecture
The predictive pipeline is built sequentially using the Keras API:
* **Input Layer:** Expects 3 features (Moisture, Temp, Sunlight).
* **Hidden Layer:** 8 densely connected neurons using **ReLU** (Rectified Linear Unit) activation to identify non-linear environmental thresholds.
* **Output Layer:** A single node running a **Sigmoid** activation function to output a clean probability curve between 0 and 1.
* **Compilation:** Optimized via Stochastic Gradient Descent (SGD) minimizing Binary Cross-Entropy loss.

## 📈 Performance & Automation Logic
The network scales inputs dynamically using Min-Max scaling to ensure fast convergence. Over a course of 365 training epochs, the network reaches **100% training accuracy** and learns to accurately flag critical dry-soil and high-temperature environmental patterns.

## 🛠️ Tech Stack & Dependencies
* **Language:** Python
* **Framework:** TensorFlow 2.x / Keras
* **Data Analysis:** Pandas, NumPy
* **Preprocessing:** Scikit-Learn (Train-Test Split)

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.