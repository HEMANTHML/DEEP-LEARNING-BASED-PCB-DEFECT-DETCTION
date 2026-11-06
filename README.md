# Deep Learning Based PCB Defect Detection

**Final Year Project Report**  
Bachelor of Technology in Computer Science and Engineering  
Alliance University, Bengaluru | May 2024

**Authors:** Nitish Akula · Hemanth Oduri  
**Supervisor:** Judeson Antony Kovilpillai  
Department of Computer Science and Engineering

---

## Overview

This project implements an automated **Printed Circuit Board (PCB) defect detection system** using deep learning. Traditional manual inspection is slow, expensive, and error-prone. We solve this by training Convolutional Neural Networks (CNNs) to classify PCB images as **defected** or **non-defect** with high accuracy.

We experiment with:
- A custom CNN architecture
- Transfer learning using pre-trained models:
  - **VGG16**
  - **ResNet50**
  - **Xception**

The **Xception** model achieved the best results, reaching **100% accuracy** on both training and test sets.

---

## Key Features

- Binary classification (defected vs non-defect)
- Transfer learning with ImageNet pre-trained weights
- Data augmentation (random flip, zoom, contrast adjustment)
- Model explainability using **LIME**
- Training callbacks (EarlyStopping, ReduceLROnPlateau)
- Ready for real-time inference integration

---

## Project Structure

DEEP-LEARNING-BASED-PCB-DEFECT-DETCTION/
├── PCB_DEFECT_RESNET.ipynb      # ResNet50 transfer learning
├── PCB_DEFECT_VGG.ipynb         # VGG16 transfer learning
├── PCB_DEFECT_XCEPTION.ipynb    # Xception transfer learning (best model)
└── README.md

## Dataset

- **Classes:** `defected` and `non-defect`
- Images were collected / manually created to include a variety of defects
- Preprocessing: resizing to 299×299, rescaling, batching
- Data augmentation applied to improve generalization

---

## Models & Results

| Model       | Approach              | Performance                          |
|-------------|-----------------------|--------------------------------------|
| Custom CNN  | From scratch          | Good baseline                        |
| VGG16       | Transfer Learning     | High accuracy                        |
| ResNet50    | Transfer Learning     | High accuracy                        |
| **Xception**| Transfer Learning     | **100%** (train & test) – Best model |

---

## Technology Stack

- **Framework:** TensorFlow + Keras
- **Models:** VGG16, ResNet50, Xception
- **Explainability:** LIME (Local Interpretable Model-agnostic Explanations)
- **Environment:** Google Colab (with Google Drive integration)
- **Other:** NumPy, Matplotlib, OpenCV, scikit-image

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/HEMANTHML/DEEP-LEARNING-BASED-PCB-DEFECT-DETCTION.git
   cd DEEP-LEARNING-BASED-PCB-DEFECT-DETCTION
   Open any of the notebooks in Google Colab.
Mount Google Drive and point to your dataset folder (structure should be):textdataset/
├── defected/
└── non-defect/
Run the cells sequentially.
The notebooks include data loading, augmentation, model definition, training, evaluation, and LIME visualization.

Nitish Akula, Hemanth Oduri. 
"Deep Learning Based PCB Defect Detection Algorithm." 
B.Tech Project Report, Alliance University, Bengaluru, May 2024.
License: This project is intended for academic and research purposes.
