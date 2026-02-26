# 🎭 Unmasking Deepfakes  
## Leveraging Deep Learning for Video Authenticity Detection  

🚀 A deep learning–based framework for detecting deepfake videos using **MTCNN + EfficientNet** architecture.

---

## 📌 Project Overview

With the rapid growth of AI-generated media, **Deepfake technology** has become a serious threat to digital authenticity. This project proposes a robust deep learning pipeline that detects whether a video is **REAL or FAKE** by:

- 🎥 Converting videos into frames  
- 🧑 Detecting and extracting faces using MTCNN  
- 🧠 Classifying faces using EfficientNet  
- 📊 Evaluating performance using Binary Cross-Entropy Loss  

The goal is to build a scalable and efficient detection system capable of identifying subtle manipulations in facial regions.

---

## 🏗️ System Architecture

### 🔄 Overall Pipeline
Video Input
↓
Frame Extraction (OpenCV)
↓
Face Detection (MTCNN)
↓
Image Preprocessing (Resize + Normalize)
↓
EfficientNet Model
↓
Binary Classification (REAL / FAKE)


---

## 🧠 Models Used

### 1️⃣ MTCNN (Face Detection)

Multi-Task Cascaded Convolutional Network used to:

- Detect faces in each frame  
- Extract bounding boxes  
- Identify facial landmarks (eyes, nose, mouth)  

This ensures the model focuses only on **important facial regions** instead of background noise.

---

### 2️⃣ EfficientNet-B0 (Classification)

EfficientNet uses **compound scaling (depth, width, resolution)** to achieve high accuracy with fewer parameters.

- ✔ Computationally efficient  
- ✔ Strong feature extraction  
- ✔ Optimized for image classification  

---

## 📂 Dataset

- 📌 **Source:** Kaggle DeepFake Dataset  
- 📦 **Format:** `.mp4` videos + metadata `.json` files  
- 🏷 **Labels:** REAL / FAKE  
- 🎞 15 FPS video frames  

### Why this dataset?

- Large scale  
- Multiple deepfake generation techniques  
- Well documented  
- Publicly available  

---

## ⚙️ Preprocessing Steps

- ✔ Convert video → frames (OpenCV)  
- ✔ Detect faces (MTCNN)  
- ✔ Resize images  
- ✔ Convert to tensors  
- ✔ Normalize (mean & std scaling)  
- ✔ Split dataset by **video ID** (not image ID) to prevent data leakage  

---

## 🏋️ Training Configuration

| Parameter | Value |
|------------|--------|
| Optimizer | Adam |
| Loss Function | Binary Cross-Entropy |
| Epochs | 15 |
| Evaluation Metric | Log Loss (BCE) |

---

## 📊 Results

🔹 **Binary Cross-Entropy (BCE): 0.45151**

- ✔ Indicates moderate prediction accuracy  
- ✔ Model successfully distinguishes real vs fake  
- ✔ Performance better than random guessing  
- ✔ Can be further improved via fine-tuning  

---

## 🔬 Key Strengths

- ✅ Efficient preprocessing pipeline  
- ✅ Face-focused detection  
- ✅ Reduced background noise impact  
- ✅ Computationally efficient architecture  
- ✅ Scalable to larger datasets  

---

## 🚀 Future Improvements

- 🔮 Integrate Transformer-based models (ViT, Swin)  
- 🔮 Use temporal features (video-level analysis)  
- 🔮 Add blink detection & inter-frame inconsistency analysis  
- 🔮 Test with larger and more diverse datasets  
- 🔮 Real-time deployment optimization  

---


