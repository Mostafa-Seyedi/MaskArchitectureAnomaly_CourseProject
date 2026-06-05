# Mask Architecture for Road Scene Understanding

This repository contains our work for the **Comprehensive Road Scene Understanding for Autonomous Driving** project.

The project focuses on semantic segmentation, panoptic segmentation, and anomaly segmentation for road scenes using **ERFNet** and **EoMT**-based mask architectures.

## Team Members

| Name | Student ID |
|---|---|
| Seyedmostafa Seyedi | s352883 |
| Soroush Khayyami | s358823 |
| Cristian Sician | s362986 |
| Fatemeh Saleh | s344410 |

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
```

## Project Steps

### 1. Semantic Segmentation

We studied **ERFNet** as a real-time semantic segmentation baseline for road-scene understanding.

### 2. Panoptic and Instance Segmentation

We reviewed the differences between semantic, instance, and panoptic segmentation to understand how different segmentation tasks represent objects and scene regions.

### 3. Mask Architectures

We studied modern mask-based segmentation architectures, including **MaskFormer**, **Mask2Former**, **DINOv2**, and **EoMT**.

### 4. EoMT Model Comparison

We compared two pretrained EoMT models:

- EoMT trained on **Cityscapes**
- EoMT trained on **COCO**

The comparison was performed on the Cityscapes validation set while considering the difference between the two datasets and their class spaces.

### 5. Fine-Tuning

We fine-tuned the COCO-trained EoMT model on the Cityscapes training set for semantic segmentation.

The fine-tuned model was evaluated on the Cityscapes validation set and compared with the original Cityscapes-trained EoMT model.

### 6. Anomaly Segmentation

We studied anomaly segmentation for road scenes, focusing on detecting unknown or out-of-distribution objects in autonomous driving environments.

### 7. Pixel-Based Baselines

We implemented pixel-based anomaly segmentation baselines using ERFNet.

The evaluated post-hoc methods include:

- MSP
- MaxLogit
- MaxEntropy

### 8. Mask-Based Baselines

We evaluated EoMT for anomaly segmentation using mask-based methods.

The evaluated methods include:

- MSP
- MaxLogit
- MaxEntropy
- RbA
- Temperature scaling

## Notebooks

| Notebook | Description |
|---|---|
| `Step_04.ipynb` | Comparison of Cityscapes-trained and COCO-trained EoMT models |
| `Step_05.ipynb` | Fine-tuning the COCO-trained EoMT model on Cityscapes |
| `step_07.ipynb` | Pixel-based anomaly segmentation baselines using ERFNet |
| `Step_08.ipynb` | Mask-based anomaly segmentation baselines using EoMT |

## Folders

| Folder | Description |
|---|---|
| `eomt/` | EoMT source code, configurations, and pretrained checkpoints |
| `eval/` | Tools for evaluation, visualization, and anomaly segmentation |
| `trained_models/` | Pretrained ERFNet models used for baseline evaluation |

## Project Links

- [Mask Architecture Anomaly Segmentation for Road Scenes](https://drive.google.com/file/d/1Vz08DHsP_mojpCTAQTR6NHVq-2rEqAZM/view?usp=sharing)
- [Comprehensive Road Scene Understanding for Autonomous Driving](https://drive.google.com/file/d/1tq5F_j_8O2vlGWbkU1ayPjYvCml1VEwr/view?usp=sharing)

## Acknowledgement

This project was developed as part of the road scene understanding and anomaly segmentation assignment.

The repository builds on the provided ERFNet and EoMT codebases for training, evaluation, visualization, and baseline comparison.
