# Dermavision System – Multimodal Skin Disease Classification

Dermavision System is a multimodal deep learning framework for skin disease classification that combines patient clinical features with skin lesion images to improve diagnostic accuracy and robustness.

The system integrates structured medical data with computer vision techniques using Artificial Neural Networks (ANN), Convolutional Neural Networks (CNN), Transfer Learning, Late Fusion, and Ensemble Learning techniques.

---

# Project Overview

Traditional skin disease diagnosis often depends on visual inspection and clinical expertise, which may lead to variability in diagnosis. Dermavision System aims to provide a more reliable AI-assisted diagnostic solution by combining:

- Clinical patient metadata
- Medical image analysis
- Multimodal fusion techniques
- Ensemble learning

The system classifies skin diseases into 6 different classes using both patient information and lesion images.

---

# Dataset

Dataset used: **PAD-UFES-20**

The dataset contains:
- Skin lesion images
- 22 patient clinical features

## Disease Classes
- BCC
- ACK
- NEV
- SEK
- SCC
- MEL

## Example Patient Features
- Age
- Gender
- Lesion location
- Skin type
- Lesion diameter

---

# System Architecture

## 1. Clinical Features Module (ANN)

Patient clinical features are:
- Cleaned and preprocessed
- Missing values handled using KNN Imputer
- Numerical data normalized
- Categorical data encoded

The processed features are then passed into an ANN model to generate prediction probabilities for the 6 disease classes.

---

## 2. Image Classification Module (CNN)

Skin disease images undergo:
- Image preprocessing
- Data augmentation
- CNN training

Transfer Learning using **MobileNet** was applied to improve performance and accelerate convergence.

### Data Augmentation Techniques
- Horizontal Flip
- Vertical Flip
- Gaussian Noise
- Color Shifting
- Random Rotation
- Zooming

The dataset expanded from:
- 2,298 images
to
- 9,192 augmented images

---

## 3. Late Fusion & Ensemble Learning

Predictions from both modalities are combined using:
- Late Fusion
- Ensemble Soft Voting

The ensemble approach improved:
- Robustness
- Reliability
- Generalization performance

---

# Technologies Used

- Python
- TensorFlow / Keras
- Scikit-learn
- NumPy
- Pandas
- OpenCV
- Matplotlib
- Flask

---

# Model Performance

| Module | Accuracy |
|---|---|
| ANN Model | 93.35% |
| CNN Baseline | 56% |
| CNN + MobileNet TL | 86.27% |
| Final Ensemble System | 98.64% |

The multimodal ensemble system significantly outperformed single-modality approaches.

---

# Features

- Multimodal Deep Learning
- ANN-based Clinical Analysis
- CNN-based Image Classification
- Transfer Learning with MobileNet
- Late Fusion Architecture
- Ensemble Learning
- Flask Deployment
- Medical Image Augmentation
- AI-assisted Clinical Diagnosis

---

# Future Improvements

- Real-time clinical deployment
- Mobile application integration
- Explainable AI (XAI)
- Larger medical datasets
- Cloud deployment

---

# Authors

Developed by Mohamed Ezzat and team members as part of a multimodal AI healthcare project.

---

# References

- PAD-UFES-20 Dataset
- TensorFlow Documentation
- MobileNet Transfer Learning
