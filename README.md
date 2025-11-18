# 🐟 Nile Tilapia Weight Prediction using Convolutional Neural Networks

![Status](https://img.shields.io/badge/status-complete-success)
![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python)
![Framework](https://img.shields.io/badge/TensorFlow-2.18-orange?logo=tensorflow)
![Conference](https://img.shields.io/badge/Paper-COTB_'25-red)
![License](https://img.shields.io/badge/license-MIT-green)

This repository contains the source code for the paper **"Weight Prediction of Nile Tilapia (Oreochromis niloticus) via Phenotype Using Convolutional Neural Networks"**, submitted to the Computer on the Beach 2025 (COTB '25) conference.

This project originated as a Final Graduation Project (TCC) at the Universidade Estadual de Maringá (UEM).

## 📄 Abstract

Biometric analysis in fish farms, such as weighing and measuring Nile tilapia, is a manual and stressful procedure for the animals and incurs significant costs, leading to growth delays and stock losses. This study investigates the application of Convolutional Neural Networks (CNNs) to estimate tilapia weight from images of its phenotype, with the aim of automating and optimizing this process. Using an existing image dataset, several CNN models were trained and evaluated. The results are promising, with some configurations achieving discrepancies of only 45–50 grams between predicted and actual weight, and a coefficient of determination ($R^2$) of 0.97. It is concluded that it is feasible to develop an efficient and accurate system to predict the weight of Nile tilapia using CNNs, with potential to increase productivity and reduce costs in fish farming.

## 📊 Key Results

The main objective was to create a regression model that could estimate the weight (in grams) of a tilapia from a 2D image. The best-performing model achieved this with high accuracy.

* **Best Model:** Nadam Optimizer (30 epochs, 30 seeds)
* **Mean Absolute Error (MAE):** **45.00 grams**
* **Coefficient of Determination ($R^2$):** **0.97**

This indicates a very strong correlation and low error, proving the method's viability for practical application in aquaculture.

---

## 🧬 Model Architecture

A Convolutional Neural Network (CNN) was designed to handle the image regression task. The architecture was built using TensorFlow/Keras and is structured as follows:

| Layer Type | Configuration | Activation |
| :--- | :--- | :--- |
| **Input** | Image (128 x 128 x 3) | - |
| **Conv2D** | 32 filters (3x3) | ReLU |
| MaxPooling | (2x2) | - |
| **Conv2D** | 64 filters (3x3) | ReLU |
| MaxPooling | (2x2) | - |
| **Conv2D** | 128 filters (3x3) | ReLU |
| MaxPooling | (2x2) | - |
| **Conv2D** | 256 filters (3x3) | ReLU |
| MaxPooling | (2x2) | - |
| **Flatten** | - | - |
| **Dense** | 512 neurons | ReLU |
| Dropout | 0.5 | - |
| **Dense** | 256
