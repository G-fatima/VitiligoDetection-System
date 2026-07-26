# Vitiligo Detection System using Digital Image Processing and KNN

## Overview

This project presents a **Vitiligo Detection System** developed using **Digital Image Processing (DIP)** and **Machine Learning** techniques. The system processes skin images, extracts meaningful features, and classifies them as **Vitiligo** or **Normal Skin** using the **K-Nearest Neighbors (KNN)** algorithm.

---

## Features

- Image preprocessing using OpenCV
- Image resizing and grayscale conversion
- Noise reduction using Gaussian Blur
- Skin region segmentation using Inverse Thresholding
- Feature extraction based on:
  - White Pixel Ratio
  - Mean Pixel Intensity
  - Standard Deviation
- Classification using K-Nearest Neighbors (KNN)
- Performance evaluation using Confusion Matrix and Accuracy Score

---

## Technologies Used

- Python
- OpenCV
- NumPy
- Scikit-learn
- Matplotlib

---

## Project Workflow

```
Input Skin Image
        │
        ▼
Image Preprocessing
(Read → Resize → Grayscale → Gaussian Blur)
        │
        ▼
Image Segmentation
(Binary Inverse Thresholding)
        │
        ▼
Feature Extraction
(White Ratio, Mean, Standard Deviation)
        │
        ▼
KNN Classification
        │
        ▼
Prediction
(Vitiligo / Normal)
```

---

## Preprocessing

The preprocessing stage includes:

- Reading the input image
- Resizing all images to **224 × 224**
- Converting the image from **BGR to Grayscale**
- Applying **Gaussian Blur** to reduce noise

---

## Segmentation

Image segmentation is performed using **Binary Inverse Thresholding**.

Threshold Value:

```
180
```

Pixels:

- Pixel ≤ 180 → White (255)
- Pixel > 180 → Black (0)

This separates the region of interest for feature extraction.

---

## Feature Extraction

Three features are extracted from each segmented image:

- **White Pixel Ratio**
- **Mean Pixel Intensity**
- **Standard Deviation**

These numerical features are used for training the machine learning model.

---

## Machine Learning Model

The project uses the **K-Nearest Neighbors (KNN)** classifier.

- Algorithm: KNN
- Number of Neighbors (K): **3**

The model predicts the class of a new image by comparing its extracted features with the three nearest training samples and assigning the majority class.

---

## Dataset Labels

| Label | Class |
|-------|--------|
| 0 | Normal Skin |
| 1 | Vitiligo |

---

## Model Evaluation

The model performance is evaluated using:

- Confusion Matrix
- Accuracy Score
- Classification Report

---


## Author

Ghulam Fatima

Computer Engineering Graduate
