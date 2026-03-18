# Face Mask Image Classification using CNN

## Project Overview
This project implements a **Convolutional Neural Network (CNN)** to classify whether a person in an image is **wearing a face mask or not**. The model is built using **TensorFlow/Keras** and trained on the **Face Mask 12K Images Dataset**.

This type of system can be used for **public safety monitoring**, especially in environments like hospitals, airports, and public transport systems.

---

## Objectives
- Build a **binary image classifier** for mask detection.
- Train a **CNN model** using TensorFlow.
- Evaluate performance using training and validation metrics.
- Save the trained model for future predictions.

---

## Dataset

Dataset used:

**Face Mask 12K Images Dataset**

Classes:

- With Mask
- Without Mask

Dataset Link: https://www.kaggle.com/datasets/ashishjangra27/face-mask-12k-images-dataset


---

##  Methodology

### 1. Data Preprocessing
- Image resizing
- Pixel normalization
- Data augmentation using `ImageDataGenerator`

### 2. Model Architecture

CNN architecture used:

Input Image (128x128x3)
↓
Conv2D + ReLU
↓
MaxPooling
↓
Conv2D + ReLU
↓
MaxPooling
↓
Flatten
↓
Dense Layer
↓
Sigmoid Output (Mask / No Mask)



---

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- KaggleHub
- Jupyter Notebook

---

## Future Improvements

- Implement Transfer Learning (ResNet / MobileNet)
- Real-time mask detection using OpenCV
- Deploy model as web application

---