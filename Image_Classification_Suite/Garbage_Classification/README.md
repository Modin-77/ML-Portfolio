# Garbage Classification using Deep Learning

## Project Overview
This project implements a **Deep Learning image classification model** designed to automate the identification of various waste materials. By leveraging Computer Vision, this system aims to enhance **recycling efficiency** and streamline waste management processes.

---

## Objectives
* **Automated Sorting:** Classify garbage images into 6 distinct categories.
* **Environmental Impact:** Distinguish between recyclable and non-recyclable materials.
* **Deep Learning Pipeline:** Build, train, and evaluate a custom CNN using **TensorFlow/Keras**.

---

## Dataset
The model is trained on the [Garbage Classification Dataset](https://www.kaggle.com/datasets/asdasdasasdas/garbage-classification), which includes:
* **Categories:** Cardboard, Glass, Metal, Paper, Plastic, and Trash.
* **Preprocessing:** Includes image resizing (128x128), pixel normalization, and real-time data augmentation.

---

## Model Architecture
The system utilizes a Sequential **Convolutional Neural Network (CNN)** optimized for feature extraction:



1.  **Input Layer:** 128x128 RGB images.
2.  **Feature Extraction:** Multiple `Conv2D` layers with `ReLU` activation followed by `MaxPooling2D` to reduce spatial dimensions.
3.  **Classification:** `Flatten` layer leading into a `Dense` hidden layer with **Dropout** for regularization.
4.  **Output Layer:** `Dense` layer with **Softmax** activation for multi-class probability.

---

## Technologies Used
* **Deep Learning:** TensorFlow, Keras
* **Data Processing:** NumPy, Scikit-learn, Pandas
* **Visualization:** Matplotlib
* **Environment:** Jupyter Notebook, KaggleHub

---

## How to Use
1. **Clone the repository** and navigate to the project folder.
2. **Install dependencies**: `pip install tensorflow numpy matplotlib`.
3. **Run the notebook**: Open `Garbage_Classification.ipynb` and execute cells to train or run inference.
