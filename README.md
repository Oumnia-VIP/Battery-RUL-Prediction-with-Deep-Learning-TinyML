# Battery-RUL-Prediction-with-Deep-Learning-TinyML

A comprehensive deep learning project for predicting Remaining Useful Life (RUL) of lithium-ion batteries using NASA's battery dataset. This project demonstrates the trade-off between model accuracy and size, comparing LSTM, FNN, and CNN architectures, with TensorFlow Lite optimization for embedded systems deployment.

# Overview
Battery health monitoring is critical for electric vehicles, smartphones, and IoT devices. This project uses machine learning to predict how many charge cycles a battery has left before failure, enabling proactive maintenance and preventing unexpected shutdowns.
Key Achievements:

✅ Accurate RUL prediction using time-series deep learning

✅ Three model architectures compared (LSTM, FNN, CNN)

✅ Model compression for embedded systems (INT8 quantization)

✅ 98.5% size reduction with minimal accuracy loss

✅ Deployment-ready TFLite models for microcontrollers

# Features

Multiple Neural Network Architectures:

- Model A: LSTM (Best Accuracy)
- Model B: Feedforward Neural Network (Smallest Size)
- Model C: 1D-CNN (Balanced Performance)


TinyML Optimization:

- TensorFlow Lite conversion
- INT8 quantization for 4x compression
- Ready for Arduino, ESP32, and embedded systems



# Dataset
This project uses the NASA Battery Dataset from the Prognostics Center of Excellence (PCoE):

- Batteries Used: B0005, B0006, B0007, B0018
- Measurements: Capacity, voltage, current, temperature, impedance
- Cycles: 150+ charge/discharge cycles per battery
- End-of-Life Threshold: 1.4 Ah


Features Extracted

- Battery capacity (Ah)
- Capacity fade over time
- Average charge/discharge voltage
- Temperature during operation
- Internal impedance
- Charge time
- Target: Remaining Useful Life (RUL) in cycles

# Model Architectures
Model A: LSTM (Long Short-Term Memory)

- Architecture: 2 LSTM layers (64, 32 units) + Dense layers
- Input: 10 timesteps × 7 features
- Strengths: Captures long-term dependencies, best accuracy
- Use Case: Cloud/server deployment

Model B: Feedforward Neural Network

- Architecture: 3 Dense layers (32, 16, 1 units)
- Input: Flattened 70 features
- Strengths: Ultra-lightweight, fast inference
- Use Case: Basic microcontrollers with limited memory

Model C: 1D-CNN (Convolutional Neural Network)

- Architecture: 2 Conv1D layers (16, 8 filters) + Dense layers
- Input: 10 timesteps × 7 features
- Strengths: Pattern detection, balanced accuracy/size
- Use Case: Recommended for embedded systems

# Installation

Python 3.8+
  
Google Colab (recommended) or Jupyter Notebook
- Upload 01_train_lstm_model.ipynb to Google Colab
- Run all cells in order
- Upload the 4 .mat files when prompted
- Results will be saved to results/ and models/ folders
