# Project Report: Multi-Task Computer Vision System using YOLOv11

**Team Members**: Pranay Karmankar, Raunak Singh, Aman Bansod, Sarvesh Pandey  
**Topic**: Deep Learning Practical - Object Detection, Classification, Pose Estimation, and OBB  
**GitHub Repository**: [https://github.com/Pranaykarmankar/practicle-3-deep-learning](https://github.com/Pranaykarmankar/practicle-3-deep-learning)

---

## 1. 🎯 Objective
The goal of this assignment is to implement a comprehensive multi-task computer vision system using the state-of-the-art **YOLOv11** architecture. The system covers four distinct tasks:
1. **Object Detection**: Identifying and localizing faces.
2. **Image Classification**: Categorizing vehicle colors.
3. **Pose Estimation**: Detecting human keypoints for Yoga pose classification.
4. **Aerial Detection**: Detecting objects (Palm Trees) from drone/satellite imagery.

## 2. 🛠️ Methodology
- **Architecture**: YOLOv11 Nano (yolo11n) - chosen for high efficiency on local hardware.
- **Framework**: Ultralytics YOLO, PyTorch.
- **Hardware**: Local execution (CPU/GPU) as per mandatory assignment compliance.
- **Datasets**: All datasets sourced from Roboflow Universe to ensure high-quality annotations.

---

## 3. 📊 Task Breakdown & Results

### Part A: Object Detection (Face Detection)
- **Dataset**: Face Detection Dataset (v27i)
- **Goal**: Detect human faces in real-time.
- **Implementation**: Trained using `yolo11n.pt` for 25 epochs.
- **Result**: Successfully achieved high mAP (mean Average Precision). Integrated with a real-time webcam testing script.
- **Output**: `Part A - Object Detection/face_detection_best.pt`

### Part B: Image Classification (Car Color)
- **Dataset**: Car Color Classification
- **Goal**: Classify the color of a vehicle from a cropped image.
- **Implementation**: Used `yolo11n-cls.pt` for 20 epochs.
- **Result**: High accuracy across multiple color classes (Red, Blue, White, etc.).
- **Output**: `Part B - Classification/car_color_best.pt`

### Part C: Pose Estimation (Yoga Poses)
- **Dataset**: Yoga Pose Prediction (v2i)
- **Goal**: Detect 14 human keypoints (skeleton) and classify the yoga pose (Tree, Plank, etc.).
- **Implementation**: Used `yolo11n-pose.pt` for 10 epochs.
- **Result**: Model successfully maps human skeletons and classifies poses accurately.
- **Output**: `Part C - Pose Estimation/yoga_pose_best.pt`

### Part D: Aerial Detection (Palm Trees)
- **Dataset**: Aerial Palm Tree Dataset
- **Goal**: Detect palm trees and regular trees from high-altitude imagery.
- **Implementation**: Used `yolo11n.pt` for 10 epochs.
- **Result**: Efficiently handled high-density detections (90+ objects per image).
- **Output**: `Part D - Oriented Bounding Boxes/aerial_palm_tree_best.pt`

---

## 4. 📂 Project Structure
```text
.
├── Part A - Object Detection/    # Face detection scripts & weights
├── Part B - Classification/      # Car color classification scripts & weights
├── Part C - Pose Estimation/     # Yoga pose skeleton scripts & weights
├── Part D - Oriented Bounding Boxes/ # Aerial detection scripts & weights
├── README.md                     # Main documentation
└── .gitignore                    # Environment control
```

## 5. ✅ Conclusion
The project demonstrates the versatility of the YOLOv11 architecture in handling diverse computer vision tasks. By utilizing local training and optimized Nano models, we achieved high-performance results suitable for real-time applications across detection, classification, and pose estimation.

---
**Submission Date**: April 24, 2026
