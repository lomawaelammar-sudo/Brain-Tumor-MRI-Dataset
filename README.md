# 🧠 Brain Tumor MRI Classification

## 📌 Project Overview

This project focuses on classifying brain MRI scans into **four categories**:

* Glioma
* Meningioma
* Pituitary Tumor
* Normal Brain

Using **deep learning and transfer learning with ResNet50V2**, the model achieves high accuracy in distinguishing between different tumor types and normal brain scans. The goal is to provide an automated system that can assist radiologists in early and accurate diagnosis.

---

## 📂 Dataset

* Source: [Brain Tumor MRI Dataset – Kaggle](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
* Classes: **4** (Glioma, Meningioma, Pituitary, Normal)
* Data split: Training, Validation, and Testing folders.
* Preprocessing: Images resized to **224×224**, normalized, and augmented (rotation, zoom, shear, flipping).

---

## ⚙️ Methodology

1. **Model**: ResNet50V2 (CNN) with ImageNet pre-trained weights.
2. **Transfer Learning**: ResNet layers frozen to act as a feature extractor.
3. **Custom Layers**: Added Flatten + Dense layers with ReLU, and a final Dense layer with softmax for 4-class classification.
4. **Training**:

   * Optimizer: Adam
   * Loss: Categorical Crossentropy
   * Callbacks: EarlyStopping (patience = 5)
   * Epochs: 20 (with early stopping)
5. **Evaluation**: Accuracy, Loss curves, Confusion Matrix, and Classification Report.

---

## 📊 Results

* **Training Accuracy**: \~94%
* **Validation Accuracy**: \~92%
* **Test Accuracy**: \~92%
* Confusion matrix shows good performance across all classes.

---

## 🚀 How to Run

1. Clone this repo or download the `.ipynb` notebook.
2. Open in **Jupyter Notebook / Google Colab / Kaggle Notebook**.
3. Install required libraries if not available (`tensorflow`, `keras`, `numpy`, `matplotlib`, `scikit-learn`).
4. Run all cells to preprocess data, train the model, and evaluate results.

---

## 📌 Applications

* Medical image analysis
* Decision support system for radiologists
* Research in tumor detection using AI

---

## 📄 File Included

* `brain_tumor_classification.ipynb` → Full notebook with preprocessing, model training, and evaluation.

---
