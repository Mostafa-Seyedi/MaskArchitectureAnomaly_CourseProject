# Mask Architecture for Road Scene Understanding

This repository contains our work for the **Comprehensive Road Scene Understanding for Autonomous Driving** project.

The project focuses on semantic segmentation, panoptic segmentation, and anomaly segmentation for road scenes using **ERFNet** and **EoMT**-based mask architectures.

## Overview

The main goal of this project is to study and evaluate segmentation models for autonomous driving scenarios, with special attention to detecting anomalous or out-of-distribution objects in road scenes.

Our work includes:

- Comparing EoMT models trained on **Cityscapes** and **COCO**
- Fine-tuning the COCO-trained EoMT model on Cityscapes
- Evaluating semantic segmentation performance using mIoU
- Implementing pixel-based anomaly segmentation baselines with ERFNet
- Implementing mask-based anomaly segmentation baselines with EoMT
- Testing post-hoc anomaly methods such as MSP, MaxLogit, MaxEntropy, RbA, and temperature scaling

## Repository Structure

```text
.
├── eomt/              # EoMT source code, configurations, and checkpoints
├── eval/              # Evaluation and visualization tools for segmentation and anomaly detection
├── trained_models/    # Pretrained ERFNet models used for baseline evaluation
├── Step_04.ipynb      # EoMT model comparison on Cityscapes and COCO
├── Step_05.ipynb      # Fine-tuning the COCO-trained EoMT model
├── step_07.ipynb      # Pixel-based anomaly segmentation baselines
├── Step_08.ipynb      # Mask-based anomaly segmentation baselines
└── README.md
