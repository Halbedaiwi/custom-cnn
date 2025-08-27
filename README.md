# 🩺 Pneumonia Detection: Custom CNN vs. ResNet-50 & DenseNet-121

## 📌 Overview
This project compares the performance of a **custom convolutional neural network (CNN)** architecture (*PneumoniaNet*) with two popular pre-trained models, **ResNet-50** and **DenseNet-121**, for the task of **pneumonia detection from chest X-ray images**.  

The notebook provides a full pipeline for:
- Data loading & preprocessing  
- Model training  
- Evaluation  
- Performance comparison  

---

## 📂 Dataset
- Combines **two public chest X-ray datasets** (`chest_xray` and `chest_xray2`).  
- Images are split into **training (70%)**, **validation (20%)**, and **test (10%)** sets with stratification to maintain class balance.  
- **Data augmentation** is applied to improve generalization.  

---

## 🧠 Models

### 1. ResNet-50
- Uses PyTorch’s pre-trained **ResNet-50**.  
- Final layer replaced for **binary classification (Normal vs. Pneumonia)**.  
- Trained with **weighted loss** to address class imbalance.  

### 2. DenseNet-121
- Uses PyTorch’s pre-trained **DenseNet-121**.  
- Classifier replaced for **binary output**.  
- Trained and evaluated using the same pipeline as ResNet-50.  

### 3. PneumoniaNet (Custom CNN)
- A **custom architecture** designed for this project.  
- Consists of:
  - Convolutional, batch normalization, pooling, and dropout layers for regularization  
  - Adaptive average pooling  
  - Fully connected layers  
- Optional: **transfer learning with ResNet-18** is supported for comparison.  

---

## ⚡ Training & Evaluation
- **GPU acceleration** used if available.  
- **Weighted random sampling** and **class-weighted loss** to handle imbalance.  
- Training pipeline includes:
  - Learning rate scheduling  
  - Early stopping  
  - Gradient clipping  
- Evaluation metrics:
  - Accuracy  
  - Confusion matrix  
  - Classification report (precision, recall, F1-score)  
  - ROC AUC  

---

## 📊 Comparison
- Provides **side-by-side training and evaluation** of all three models.  
- Results include:
  - Classification metrics  
  - Confusion matrices  
- Enables **direct comparison** of the custom CNN against ResNet-50 and DenseNet-121.  

---

## 🚀 Usage
1. Clone the repository and place the datasets in the specified paths.  
2. Open the notebook in **Jupyter Notebook** or **VS Code**.  
3. Run each section to train and evaluate the models.  
4. Review the metrics and outputs for model comparison.  

---

## ✅ Results
- A well-regularized **custom CNN** can approach or match the performance of deeper, pre-trained models in medical imaging tasks.  
- The code is **modular** and can be adapted for other **binary image classification** problems.  

---
