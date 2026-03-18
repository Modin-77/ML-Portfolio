# Helmet Detection System (YOLOv8 Object Detection)

A computer vision solution designed for real-time safety monitoring in traffic and industrial environments. This project leverages the **YOLOv8** (You Only Look Once) architecture to detect and classify individuals based on helmet usage.

## Project Overview
* **Objective:** Detect and categorize persons into `With Helmet` or `Without Helmet`.
* **Model:** YOLOv8 Nano (yolov8n.pt) for high-speed, real-time inference.
* **Architecture:** State-of-the-art Object Detection utilizing bounding box predictions.
* **Applications:** Traffic law enforcement, construction site safety, and smart surveillance.

## Data Engineering & Preprocessing
A critical part of this project was the transformation of the raw Kaggle dataset into a model-ready format:
1. **Annotation Conversion:** Automated the conversion of **Pascal VOC (.xml)** annotations into **YOLO (.txt)** format.
2. **Normalization:** Bounding box coordinates were normalized $(x_{center}, y_{center}, width, height)$ between 0 and 1.
3. **Data Split:** Implemented an 80/20 Train-Validation split with a structured directory for images and labels.



## Training Configuration
* **Framework:** Ultralytics YOLOv8
* **Input Size:** 640x640 pixels
* **Epochs:** 30
* **Batch Size:** 16
* **Pretrained Weights:** COCO dataset (transfer learning)

## Performance Results
The model demonstrates strong localization and classification capabilities:

| Metric | Score |
| :--- | :---: |
| **mAP@50** | 0.85 – 0.92 |
| **Precision** | 0.85+ |
| **Recall** | 0.80+ |

### Key Insight
High **mAP@50** scores confirm the model's reliability in identifying safety gear, though further refinement in diverse lighting conditions could improve the mAP@50-95 threshold.

## Quick Inference
```python
from ultralytics import YOLO

# Load the trained weights
model = YOLO("helmet_detection_final.pt")

# Run detection
results = model.predict(source="test_image.jpg", conf=0.25, show=True)
