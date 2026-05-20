# Face Recognition Using PCA Eigenfaces and SVM Classifier

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?style=for-the-badge&logo=opencv)
![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikitlearn)
![Status](https://img.shields.io/badge/Project-Completed-success?style=for-the-badge)

</div>

---

# Overview

This project implements a Face Recognition System using:

- Principal Component Analysis (PCA)
- Eigenfaces
- Support Vector Machine (SVM)

The system recognizes human faces by extracting important facial features using PCA and classifying them using SVM.

The project demonstrates how high-dimensional facial image data can be reduced into a lower-dimensional feature space while preserving important facial characteristics.

---

# Objectives

- To implement facial recognition using PCA
- To generate Eigenfaces
- To reduce image dimensionality
- To classify faces using SVM
- To analyze recognition accuracy for different PCA dimensions
- To implement imposter detection
- To evaluate classifier performance

---

# Features

- Face Image Preprocessing
- Histogram Equalization
- Mean Face Generation
- Eigenface Extraction
- PCA Dimensionality Reduction
- SVM Based Face Classification
- Accuracy vs k Analysis
- Imposter Detection
- Confusion Matrix
- Classification Report

---

# Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| OpenCV | Image Processing |
| NumPy | Numerical Computation |
| Matplotlib | Visualization |
| Scikit-learn | PCA and SVM |
| Google Colab | Development Environment |

---

# Dataset Structure

```text
dataset/
└── faces/
    ├── Aamir/
    ├── Ajay/
    ├── Akshay/
    ├── Alia/
    ├── Amitabh/
    ├── Deepika/
    ├── Disha/
    ├── Farhan/
    └── Ileana/
```

Each folder contains multiple grayscale face images.

---

# Project Workflow

```text
Load Dataset
      ↓
Image Preprocessing
      ↓
Mean Face Calculation
      ↓
Mean Centering
      ↓
Apply PCA
      ↓
Generate Eigenfaces
      ↓
Reduce Dimensionality
      ↓
Train SVM Classifier
      ↓
Face Recognition
      ↓
Performance Evaluation
      ↓
Imposter Detection
```

---

# Methodology

# 1. Image Preprocessing

The following preprocessing steps are applied:

- Grayscale Conversion
- Histogram Equalization
- Image Resizing (100×100)
- Image Flattening
- Normalization

---

# 2. Mean Face Calculation

The average face of the training dataset is calculated.

## Formula

\[
\mu = \frac{1}{N}\sum_{i=1}^{N} x_i
\]

Where:
- \( \mu \) = Mean Face
- \( x_i \) = Face Vector
- \( N \) = Number of Images

---

# 3. Mean Centering

Mean face is subtracted from all training images.

## Formula

\[
X_{centered} = X - \mu
\]

---

# 4. Principal Component Analysis (PCA)

PCA is used for:
- Feature extraction
- Dimensionality reduction
- Eliminating redundant information

---

# 5. Eigenfaces

Eigenvectors generated from PCA are known as Eigenfaces.

Eigenfaces represent:
- Important facial structures
- Variations among faces
- Dominant facial features

---

# 6. SVM Classification

Support Vector Machine (SVM) classifier is trained using PCA features.

## Why SVM?

SVM works efficiently for:
- Small datasets
- High-dimensional data
- Face recognition problems

---

# 7. Imposter Detection

If prediction confidence is below threshold:

```python
if confidence < 0.6:
    print("Unknown Person")
```

Then the person is classified as unknown.

---

# Results

| Metric | Value |
|---|---|
| Recognition Accuracy | ~68% |
| PCA Components | 150 |
| Classifier | SVM |
| Image Size | 100×100 |

---

# Accuracy vs PCA Components

Different PCA component values were tested.

| PCA Components (k) | Observation |
|---|---|
| 10 | Lower Accuracy |
| 50 | Improved Accuracy |
| 100 | Better Performance |
| 125 | High Accuracy |
| 150 | Best Accuracy |

---

# Advantages

- Efficient dimensionality reduction
- Lower computational cost
- Faster recognition
- Good performance on small datasets
- Easy implementation

---

# Limitations

- Sensitive to lighting conditions
- Accuracy depends on image quality
- Less robust compared to deep learning methods

---

# Applications

- Biometric Authentication
- Security Systems
- Attendance Systems
- Surveillance Systems
- Access Control
- Criminal Identification

---

# Future Scope

This project can be enhanced using:

- Convolutional Neural Networks (CNN)
- Deep Learning
- Real-time webcam recognition
- Larger datasets
- GUI implementation
- Web deployment

---

# Installation

## Clone Repository

```bash
git clone https://github.com/your-username/Face-Recognition-Using-PCA-and-SVM.git
```

---

# Open Project Directory

```bash
cd Face-Recognition-Using-PCA-and-SVM
```

---

# Install Required Libraries

```bash
pip install numpy matplotlib opencv-python scikit-learn
```

---

# Run the Project

Open Jupyter Notebook or Google Colab and run:

```text
FaceRecognition_PCA_ANN.ipynb
```

---

# Project Structure

```text
Face-Recognition-Using-PCA-and-SVM/
│
├── FaceRecognition.ipynb
├── README.md
├── models/
│   ├── FaceRecognition_SVM.pkl
│   ├── PCA_Model.pkl
│   └── Label_Map.pkl
│
└── dataset/
```

---

# Learning Outcomes

This project helped in understanding:

- Computer Vision
- Image Processing
- PCA
- Eigenfaces
- Dimensionality Reduction
- Machine Learning
- SVM Classification
- Model Evaluation

---

# Conclusion

This project successfully implemented a complete face recognition system using PCA Eigenfaces and SVM classifier.

PCA effectively reduced the dimensionality of facial images while preserving important facial information. The SVM classifier achieved satisfactory recognition performance and successfully classified different individuals.

The project demonstrates the practical implementation of machine learning and dimensionality reduction techniques in biometric recognition systems.

---

# Author

## Himanshu Ahirrao

---

# License

This project is developed for educational and academic purposes.

---
