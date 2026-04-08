# W-Net: Lightweight Medical Image Segmentation
基于 PyTorch 实现的轻量级视网膜血管分割网络

## 📖 Introduction
This repository contains the official implementation of **W-Net**, a highly lightweight, two-stage segmentation network designed for resource-constrained environments (e.g., edge devices and mobile terminals). The model achieves state-of-the-art performance on the DRIVE dataset with exceptionally low computational overhead.

## ✨ Architectural Innovations
Based on the standard U-Net architecture, W-Net introduces two key modifications:
1. **1×1 Residual Shortcut**: Mitigates gradient vanishing during deep feature extraction.
2. **Skip Feature Convolution Bridge (Conv-Bridge)**: Bridges the semantic gap between the encoder's low-level features and the decoder's high-level features.

## 🚀 Performance on DRIVE Dataset
* **Parameters**: ~0.07M (Model weight: 0.3MB)
* **AUC**: 0.9810
* **Dice**: 0.8284
* **Accuracy**: 0.9554
* **Loss Function**: BCE Loss + Dice Loss

## 🛠️ Tech Stack & Pipeline
* **Framework**: PyTorch
* **Pipeline**: Custom `Dataset` and `Transform` for data augmentation, learning rate schedulers, logging, and batch inference scripts. All implemented from scratch.

## 📄 Research Paper
For detailed ablation studies, network topology, and visualizations, please refer to the uploaded `Course_Paper.pdf`.
