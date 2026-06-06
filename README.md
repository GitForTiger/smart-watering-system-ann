# Smart Watering Automation using Artificial Neural Network

This repository demonstrates a smart irrigation automation system powered by an Artificial Neural Network (ANN). The project predicts whether a crop requires watering based on environmental telemetry data such as soil moisture, temperature, and sunlight exposure.

The objective is to move beyond traditional fixed-threshold irrigation systems and develop an intelligent, data-driven approach that can optimize water usage while maintaining healthy crop conditions.

---

## 🚀 Project Workflow

### 1. Data Collection & Feature Engineering
Environmental telemetry data is collected and structured into a feature matrix containing:

- Soil Moisture Level
- Ambient Temperature
- Sunlight Exposure Duration

The target variable is:

- **needs_water**
  - `1` → Watering Required
  - `0` → No Watering Required

### 2. Data Preprocessing

- Checked dataset consistency and feature distributions.
- Applied Min-Max Scaling to normalize all input features.
- Split the dataset into training and testing sets.
- Prepared the data for efficient neural network training.

### 3. Model Development

A feed-forward Artificial Neural Network was built using TensorFlow/Keras.

#### Input Layer
- Accepts three environmental features:
  - Soil Moisture
  - Temperature
  - Sunlight Hours

#### Hidden Layer
- 8 Dense Neurons
- ReLU Activation Function
- Learns non-linear relationships between environmental variables

#### Output Layer
- 1 Dense Neuron
- Sigmoid Activation Function
- Produces a probability indicating whether watering is required

#### Model Compilation
- Optimizer: Stochastic Gradient Descent (SGD)
- Loss Function: Binary Cross-Entropy
- Evaluation Metric: Accuracy

---

## 🧠 Feature Description

| Feature | Description |
|----------|-------------|
| Soil Moisture | Volumetric soil water content (0.0 – 1.0) |
| Temperature | Ambient temperature in °C |
| Sunlight Hours | Duration of sunlight exposure |
| needs_water | Binary target indicating watering requirement |

---

## 📊 Model Performance

The ANN was trained over **365 epochs** and successfully learned the underlying environmental patterns associated with crop water requirements.

### Key Results

- Achieved **100% training accuracy**
- Successfully identified dry-soil conditions requiring irrigation
- Learned complex interactions between moisture, temperature, and sunlight exposure
- Demonstrated the potential of AI-driven irrigation systems over static rule-based approaches

### Automation Logic

The trained model receives environmental sensor readings and predicts whether watering should be triggered.

Example Decision Patterns:

| Soil Moisture | Temperature | Sunlight Hours | Prediction |
|---------------|------------|---------------|------------|
| Low | High | High | Water Required |
| High | Moderate | Moderate | No Water Required |
| Medium | High | Long Exposure | Water Required |

---

## 🌱 Real-World Applications

This project can serve as the foundation for:

- Smart Agriculture Systems
- IoT-Based Irrigation Controllers
- Greenhouse Automation
- Precision Farming Solutions
- Water Conservation Initiatives

By integrating the trained ANN with soil and weather sensors, irrigation can be automated in real time, reducing water waste and improving crop health.

---

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- TensorFlow
- Keras
- Scikit-Learn

---

## 📂 Project Structure

```text
├── Smart_Watering_ANN.ipynb
├── dataset.csv
├── README.md
```

---

## 🎯 Future Improvements

- Incorporate additional environmental parameters such as:
  - Humidity
  - Rainfall Forecast
  - Wind Speed
  - Soil Nutrient Levels

- Deploy the model on:
  - Raspberry Pi
  - ESP32
  - Arduino-compatible IoT systems

- Integrate cloud monitoring dashboards for real-time irrigation analytics.

- Develop a mobile application for remote monitoring and control.

---

## 🌟 Conclusion

This project demonstrates how Artificial Neural Networks can be applied to smart agriculture by learning complex environmental patterns and making intelligent irrigation decisions. The approach showcases the potential of combining Deep Learning and IoT technologies to build sustainable, resource-efficient farming solutions.

---
