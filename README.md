# 🔍 Surface Defect Image Classification  

<p align="center">
  <b>Deep Learning–Based Automated Industrial Defect Detection</b>
</p>

---

## 📌 Overview

This project implements a Deep Convolutional Neural Network (CNN) to automatically detect and classify surface defects in industrial steel materials using the NEU-DET dataset.

The system is designed to improve manufacturing quality control by replacing manual inspection with a scalable and consistent deep learning solution.

---

## 🎯 Objective

- Automate detection of steel surface defects  
- Improve inspection speed and reliability  
- Build a structured end-to-end image classification pipeline  
- Demonstrate practical industrial AI implementation  

---

## 📂 Dataset

**Dataset:** NEU-DET (Northeastern University Surface Defect Database)

The dataset consists of grayscale images of hot-rolled steel strips categorized into six defect classes:

- Crazing  
- Inclusion  
- Patches  
- Pitted Surface  
- Rolled-in Scale  
- Scratches  

### Dataset Preparation

- Extracted dataset from `archive.zip`
- Organized into structured directories
- Resized and normalized images
- Split into training and validation datasets
- Batched and shuffled using TensorFlow data pipeline

---

## 🧠 Model Architecture

The project uses a Deep Convolutional Neural Network (CNN) for multi-class classification.

### Architecture Overview

```
Input (224x224)
   ↓
Conv2D + ReLU
   ↓
MaxPooling
   ↓
Conv2D + ReLU
   ↓
MaxPooling
   ↓
Fully Connected Layer
   ↓
Dropout
   ↓
Softmax (6 Classes)
```

### Design Choices

- ReLU activation for non-linearity  
- Softmax for multi-class probability output  
- Dropout for regularization  
- Categorical Cross-Entropy loss  
- Adam optimizer for stable convergence  

The architecture balances representational power and computational efficiency for practical industrial deployment scenarios.

---

## 🔄 Data Pipeline

1. Dataset extraction  
2. Directory-based image loading  
3. Image resizing and normalization  
4. Data augmentation (flip, rotation, zoom)  
5. Train–validation split  
6. Model training and evaluation  

Data augmentation improves generalization and reduces overfitting.

---

## 🏋️ Training Configuration

| Parameter | Value |
|------------|--------|
| Framework | TensorFlow / Keras |
| Optimizer | Adam |
| Loss | Categorical Cross-Entropy |
| Epochs | 20 |
| Batch Size | 16 |
| Hardware | Google Colab (GPU) |

---

## 📊 Results

### Overall Performance

| Metric   | Training | Validation |
|----------|----------|------------|
| Accuracy | 98.90%   | 96.11%     |
| Loss     | 0.53     | 0.68       |

Training and validation curves were monitored to ensure stable convergence and minimal overfitting.

---

## 📈 Evaluation

- Accuracy tracking during training  
- Training vs validation loss visualization  
- Confusion matrix generation  
- Multi-class Precision, Recall, and F1-score analysis  

The confusion matrix demonstrates strong diagonal dominance, indicating high class-wise prediction reliability.

---

## 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| Language | Python |
| Deep Learning | TensorFlow / Keras |
| Numerical Computing | NumPy |
| Visualization | Matplotlib |
| Environment | Google Colab |

---

## 📁 Project Structure

```
Surface_Defect_Image_Classification/
│
├── NEU-DET/
│   ├── train/
│   ├── validation/
│   └── annotations/
│
├── Surface_Defect_ImgClassification_devlopment.ipynb
└── README.md
```

---

## ⚙️ Installation

```bash
pip install tensorflow numpy matplotlib
```

If using Google Colab, most dependencies are pre-installed.

---

## ▶️ Usage (Google Colab)

1. Upload `Surface_Defect_ImgClassification_devlopment.ipynb`  
2. Upload `archive.zip`  
3. Run all cells sequentially:
   - Dataset extraction  
   - Data loading & preprocessing  
   - Model building  
   - Training  
   - Evaluation  

4. Monitor training accuracy and loss curves.

---

## 🚀 Future Improvements

- Hyperparameter optimization  
- Transfer learning with pretrained architectures (ResNet / EfficientNet)  
- Class imbalance handling  
- Deployment using FastAPI  
- Edge-device model quantization  
- Real-time inference integration  

---

## 📌 Applications

- Automated steel surface inspection  
- Smart manufacturing systems  
- Industrial quality control automation  
- Real-time visual inspection systems  

---

## 👤 Author : Kunal Kongari (IISc Bangalore)

Developed as part of a graduate-level deep learning and computer vision project focused on industrial AI applications.
