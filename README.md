# 🧠 Weld Defect Detection using Deep Learning

## 🔹 Overview
This repository presents an **AI-powered welding defect detection system** built using **YOLOv8, TensorFlow, and OpenCV**.  
It automatically identifies and classifies welding surface defects such as:

- **Porosity**
- **Spatter**
- **Undercut**
- **Lack of Fusion**
- **Good Welds**

The goal is to enhance **industrial quality assurance** by automating visual inspection processes and reducing manual error.

---

## 🧰 Tech Stack
- **Python 3.9+**
- **YOLOv8 (Ultralytics)**
- **TensorFlow / PyTorch**
- **OpenCV**
- **FastAPI** for deployment
- **LabelImg** for dataset annotation
- **Matplotlib, Pandas, NumPy** for analysis and visualization

---

## 📸 Dataset Samples

| Good Weld | Porosity | Undercut |
|------------|-----------|-----------|
| ![](dataset_samples/weld_good.jpg) | ![](dataset_samples/weld_porous.jpg) | ![](dataset_samples/weld_undercut.jpg) |

> *The full dataset cannot be shared publicly due to industrial confidentiality; however, sample images are included.*

---

## ⚙️ Model Overview

| Component | Description |
|------------|--------------|
| **Model Type** | YOLOv8 (Custom trained) |
| **Input Image Size** | 640x640 |
| **Training Split** | 85% Train / 15% Validation |
| **Defect Classes** | 5 (Porosity, Spatter, Undercut, Lack of Fusion, Good Weld) |
| **Accuracy (mAP)** | ~90% on validation dataset |

---

## 🚀 Training Pipeline

1. Annotated dataset using **LabelImg** (bounding boxes for each defect type).  
2. Preprocessed data using **OpenCV** and **NumPy**.  
3. Configured **YOLOv8** training YAML file.  
4. Trained on GPU (Google Colab) for 100 epochs.  
5. Evaluated using precision, recall, F1-score, and mAP metrics.

---

## 🌐 Deployment
The trained model was deployed using **FastAPI** for **real-time inspection**.

- Upload an image via API or web interface.
- The model returns bounding boxes, class labels, and confidence scores.
- Integrated for use in **industrial inspection dashboards**.

**Sample API Endpoint:**
