# 🧠 Brain Tumor Classification using Deep Learning (ResNet50)

This project presents an automated system for classifying brain MRI images into four categories: **Glioma**, **Meningioma**, **Pituitary Tumor**, and **No Tumor** using a **ResNet50**-based deep learning model. The system aims to support radiologists and healthcare professionals in early and accurate diagnosis of brain tumors.

---

## 📝 Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [How to Run](#how-to-run)
- [Results](#results)
- [Future Scope](#future-scope)
- [References](#references)

---

## 📌 Project Overview

Brain tumors can significantly impact human health, and early detection is critical. This project automates the classification of brain tumors in MRI images using transfer learning with ResNet50. It improves diagnostic efficiency by reducing manual effort and increasing accuracy through deep learning.

Key features:
- Classification of MRI images into four tumor categories.
- Preprocessing and data augmentation for performance boost.
- Deployment-ready with Google Colab and Gradio UI.

---

## 🎯 Objectives

- Classify MRI scans into:
  - **Glioma**
  - **Meningioma**
  - **Pituitary Tumor**
  - **No Tumor**
- Achieve high classification accuracy using ResNet50.
- Provide a simple interface for uploading and predicting new images.
- Enable fast, automated diagnosis to aid healthcare decision-making.

---

## 🧠 Model Architecture

- **Base Model:** ResNet50 (pre-trained on ImageNet).
- **Transfer Learning:** Custom dense layers on top of ResNet50.
- **Loss Function:** Categorical Crossentropy.
- **Optimizer:** Adam.
- **Accuracy Metric:** Validation Accuracy & Loss.
- **Training Epochs:** 10.
- **Augmentations:** Rotation, Zoom, Flip, Shift.

---

## 🗂️ Dataset

- **Source:** [Kaggle - Brain Tumor Classification MRI Dataset](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri)
- **Classes:** Glioma, Meningioma, Pituitary Tumor, No Tumor
- **Preprocessing:** 
  - Image resizing to 224x224.
  - Normalization.
  - Augmentations using `ImageDataGenerator`.

---

## 🛠️ Technologies Used

| Tool/Library        | Purpose                      |
|---------------------|------------------------------|
| Python 3.x          | Programming Language         |
| TensorFlow / Keras  | Deep Learning Framework      |
| OpenCV / PIL        | Image Processing             |
| NumPy / Pandas      | Data Manipulation            |
| Matplotlib / Seaborn| Data Visualization           |
| Gradio              | Web Interface for Inference  |
| Google Colab        | Model Training & Deployment  |

---

## 🚀 How to Run

1. **Download Dataset:**
```python
import kagglehub
brain_tumor_path = kagglehub.dataset_download('sartajbhuvaji/brain-tumor-classification-mri')
