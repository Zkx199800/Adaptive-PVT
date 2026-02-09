# Adaptive-PVT: Adaptive Feature Fusion and Alignment for Medical Image Segmentation

[![PyTorch](https://img.shields.io/badge/PyTorch-1.10+-EE4C2C?logo=pytorch&logoColor=white)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Generic badge](https://img.shields.io/badge/Status-SOTA-brightgreen.svg)](https://github.com/Zkx199800/Adaptive-PVT)

**Adaptive-PVT** is a hierarchical Vision Transformer-based framework for precise medical image segmentation. By introducing adaptive alignment and boundary enhancement mechanisms, it overcomes spatial inconsistencies and semantic gaps typical in complex anatomical structures.

[Image of Adaptive-PVT network architecture with AFUFA and ABE modules]

---

## 🔥 Core Modules

* **AFUFA (Adaptive Feature Unfolding and Alignment):** A guided-filtering-based alignment module that effectively bridges the spatial gap between high-resolution structural features and low-resolution semantic features.
* **ABE (Adaptive Boundary Enhancement):** Dynamically refines boundary predictions, addressing the ambiguity often found in lesion and organ edges.
* **Hierarchical Fusion:** Optimized PVT-V2 backbone to capture long-range dependencies while maintaining computational efficiency.

---

## 📂 Dataset Preparation

We evaluated our model on five major benchmarks. Please download the datasets from the official links and organize them as follows:

### 1. Download Links
- **Synapse (Multi-organ CT):** [Official Link](https://www.synapse.org/#!Synapse:syn3193805/wiki/217789)
- **ACDC (Cardiac MRI):** [Official Link](https://www.creatis.insa-lyon.fr/Challenge/acdc/)
- **Kvasir-SEG (Polyp):** [Official Link](https://datasets.simula.no/kvasir-seg/)
- **EndoScene (Polyp):** [Official Link](http://adas.cvc.uab.es/endoscene)
- **ISIC (Skin Lesion):** [Official Link](https://challenge.isic-archive.com/data/)

### 2. Directory Structure
```text
data/
├── Synapse/
│   ├── train_npz/            # Training slices (.npz)
│   ├── test_vol_h5/          # Testing volumes (.h5)
│   ├── all.lst
│   ├── test_vol.txt
│   └── train.txt
├── ACDC/
│   ├── training/             # 2D slices (.h5)
│   └── testing/              # 3D volumes (.h5)
├── Kvasir-SEG/               # Polyp images and masks (.jpg)
│   ├── train/
│   │   ├── images
│   │   └── masks
│   └── val/
│   │   ├── images
│   │   └── masks
├── EndoScene/               # Polyp images and masks (.png)
│   ├── train/
│   │   ├── images
│   │   └── masks
│   └── val/
│   │   ├── images
│   │   └── masks
├── ISIC2017/               # Skin lesion images and masks (.png)
│   ├── train/
│   │   ├── images
│   │   └── masks
│   └── val/
│   │   ├── images
│   │   └── masks
├── ISIC2018/               # Skin lesion images and masks (.png)
│   ├── train/
│   │   ├── images
│   │   └── masks
│   └── val/
│   │   ├── images
│   │   └── masks
