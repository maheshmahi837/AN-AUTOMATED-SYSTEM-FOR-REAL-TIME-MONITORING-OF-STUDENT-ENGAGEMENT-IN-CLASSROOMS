# Automated Student Motivation Monitoring System

An end-to-end deep learning framework for real-time classroom engagement and motivation monitoring using computer vision, temporal modeling, and multimodal learning.

---

## Overview

This project presents an automated classroom analytics system designed to monitor student engagement in physical classroom environments. The framework combines intelligent video acquisition, face tracking, clustering, and deep learning-based engagement classification to analyze student attention and emotional states over time.

The system is designed to operate in real classroom conditions with challenges such as:

* Occlusions
* Illumination variations
* Pose changes
* Multi-student tracking
* Motion blur

---

## System Pipeline

### 1. Automated Video Acquisition

* PTZ camera control using VISCA-over-IP
* Structured classroom scanning
* RTSP-based video streaming and recording using FFmpeg

### 2. Face Detection and Quality Filtering

* YOLO-based face detection
* Blur filtering using Laplacian variance
* Small-face removal
* Occlusion-aware face validation

### 3. Face Embedding and Clustering

* Deep facial embeddings extraction
* DBSCAN clustering for student identity grouping
* Consistent student tracking across frames

### 4. Engagement Classification

#### Baseline Model

* EfficientNet-B0 backbone (EmotiEffLib)
* Temporal Attention Pooling
* Binary engagement classification

#### Proposed Model

* Multimodal Temporal Convolutional Network (TCN)
* Gated fusion of face and pose features
* Temporal sequence modeling using Conv1D layers

---

## Dataset

The project uses the DAiSEE dataset for engagement classification.

### Engagement Labels

* Very Low
* Low
* High
* Very High

The labels are converted into a binary engagement setup for training and evaluation.

---

## Key Features

* Real-time classroom monitoring
* Automated PTZ camera control
* YOLO-based face extraction
* DBSCAN-based student clustering
* Temporal attention modeling
* TCN-based sequence learning
* Pose-guided multimodal fusion
* Timestamp-wise engagement reporting
* Emotion-aware analytics

---

## Technologies Used

* Python
* PyTorch
* OpenCV
* YOLO
* MediaPipe
* EmotiEffLib
* Scikit-learn
* FFmpeg
* NumPy
* Pandas

---

## Model Performance

| Model                       | Accuracy |
| --------------------------- | -------- |
| EfficientNet-B0 + Attention | 60.82%   |
| Proposed Multimodal TCN     | 66.49%   |

The proposed TCN-based architecture demonstrates improved temporal modeling and stronger discriminative capability compared to the baseline attention-based model.

---

## Results

The system generates:

* Confusion matrices
* ROC curves
* Precision-recall curves
* Training dynamics plots
* Timestamp-wise engagement reports
* Student emotion summaries

---

## Project Structure

```bash
├── dataset/
├── preprocessing/
├── clustering/
├── models/
├── training/
├── inference/
├── outputs/
├── plots/
└── README.md
```

---

## Future Work

* Transformer-based temporal architectures
* Multi-camera classroom coverage
* Audio-visual engagement fusion
* Real-time deployment optimization
* Adaptive learning analytics

---

## Author

Mahesh Kusireddy
M.Tech — Signal Processing and Machine Learning
Indian Institute of Technology Kharagpur

---

## License

This project is intended for academic and research purposes.
