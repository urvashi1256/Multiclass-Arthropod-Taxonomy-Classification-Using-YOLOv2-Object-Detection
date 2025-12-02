# 🐛 Multiclass Arthropod Taxonomy Classification Using YOLOv2

Real-time object detection and classification of 7 arthropod orders using YOLOv2 deep learning model.

## 🎯 Project Overview

This project trains **YOLOv2** (latest Ultralytics implementation) on the **Arthropod Taxonomy Dataset** to detect and classify insects across 7 orders:
- **Araneae** (Spiders) 
- **Coleoptera** (Beetles)
- **Diptera** (Flies)
- **Hemiptera** (True bugs)
- **Hymenoptera** (Bees, wasps)
- **Lepidoptera** (Butterflies, moths)
- **Odonata** (Dragonflies)

## 📊 Results
- **mAP@50**: 0.678
- **mAP@50-95**: 0.519
- **Precision**: 0.71
- **Recall**: 0.618

## 🛠️ Tech Stack
YOLOv2 (Ultralytics) | PyTorch | Python | OpenCV
Kaggle Dataset | GPU Training (Tesla T4)

## 🚀 Quick Start

1. **Clone repo**

git clone https://github.com/urvashi1256/Multiclass-Arthropod-Taxonomy-Classification-Using-YOLOv2-Object-Detection
cd Multiclass-Arthropod-Taxonomy-Classification-Using-YOLOv2-Object-Detection


2. **Install dependencies**

pip install ultralytics torch torchvision opencv-python

3. **Download dataset** (Kaggle required)

Follow dataset conversion notebook
jupyter notebook dataset_preparation.ipynb


4. **Train model**

yolo train model=yolov2n.pt data=arthropods.yaml epochs=50 imgsz=640

5. **Run inference**
yolo predict model=best.pt source="path/to/images"

## 📁 Project Structure
├── dataset/ # Converted YOLO format dataset
├── runs/detect/ # Training results & visualizations
├── vertopal.com_yolo_v2.pdf # Complete project notebook
├── arthropods.yaml # Dataset config
└── README.md


## 📈 Performance Metrics
| Class       | Precision | Recall | mAP@50 | mAP@50-95 |
|-------------|-----------|--------|--------|-----------|
| Araneae     | 0.871     | 0.681  | 0.771  | 0.609     |
| Coleoptera  | 0.479     | 0.675  | 0.636  | 0.479     |
| Odonata     | 0.886     | 0.881  | 0.919  | **0.780** |

## 🎥 Demo Results
![Detection Results](runs/detect/yolov11custom4/val_batch0_pred.jpg)

## 🔗 Colab Notebook
[![Open In Colab](https://colab.research.google.com/drive/1AwRyNbvAiUBgFMiL0lDjVA1HCInZmIzm?usp=sharing)

## 📝 Citation

@project{arthropod-yolo2025,
author = {Urvashi Salonia},
title = {Multiclass Arthropod Taxonomy Classification Using YOLOv2},
year = {2025}
}

**Built with ❤️ for insect classification research**