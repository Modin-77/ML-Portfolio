# Computer Vision Suite

This suite demonstrates a range of Deep Learning capabilities—from simple **Binary Classification** to complex **Real-Time Object Detection (YOLOv8)**. These projects address real-world challenges in workplace safety, public health, and environmental sustainability.

---

## Project Portfolio

### 1. Helmet Detection (Object Detection)
* **Architecture:** YOLOv8 (Nano)
* **Task:** Detect and locate individuals with/without helmets using bounding boxes.
* **Key Tech:** XML-to-YOLO annotation conversion, mAP evaluation.
* **[View Project](./HelmetDetectionYOLOv8)**

### 2. Face Mask Detection (Classification)
* **Architecture:** CNN (TensorFlow/Keras)
* **Task:** Binary classification of 12,000+ images to verify mask compliance.
* **Key Tech:** ImageDataGenerator for augmentation, Sigmoid activation.
* **[View Project](./Face_Mask_Image_Classification)**

### 3. Garbage Classification (Multi-class)
* **Architecture:** CNN (TensorFlow/Keras)
* **Task:** Sorting waste into 6 categories (Glass, Paper, Metal, Plastic, etc.).
* **Key Tech:** Multi-class Softmax output, Automated waste sorting logic.
* **[View Project](./Garbage_Classification)**

---

## Technical Implementation
Across this suite, the following CV principles were applied:

| Feature | Description |
| :--- | :--- |
| **Preprocessing** | Image resizing (128x128 / 640x640), Normalization, and Augmentation. |
| **Modeling** | Sequential CNNs for classification and YOLOv8 for spatial detection. |
| **Optimization** | Dropout layers to prevent overfitting and EarlyStopping for training efficiency. |
| **Evaluation** | Accuracy/Loss curves for CNNs and mAP (mean Average Precision) for YOLO. |



[Image of Convolutional Neural Network layers]


## Global Tech Stack
* **Frameworks:** TensorFlow, Keras, Ultralytics (YOLOv8)
* **Processing:** OpenCV, PIL, NumPy
* **Analysis:** Matplotlib, Scikit-learn, Seqeval
* **Data Source:** Kaggle Datasets via `kagglehub`
