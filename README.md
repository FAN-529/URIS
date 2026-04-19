# Siamese Network-based Intraoperative Video Analysis for Cataract Surgical Instrument Recognition
Undergraduate Research and Innovation Scheme (URIS) | EEE Department

## Project Overview
This project focuses on **intraoperative surgical instrument recognition for cataract surgery** based on Siamese Network. By integrating YOLOv10 for real‑time instrument extraction and advanced multi‑modal embedding models, it solves the problems of background interference, similar‑instrument misclassification and information redundancy in traditional frame‑by‑frame detection, and significantly improves recognition accuracy and generalization.

This code library fully implements the TTT-UNet model, which integrates Test-Time Training (TTT) layers into the conventional U-Net architecture to resolve the core limitations in biomedical image segmentation: the inability of CNNs to effectively capture long-range dependencies and the excessively high computational cost of Transformers.

## Core Features
- Dual‑branch Siamese Network for discriminative instrument embedding learning
- YOLOv10 end‑to‑end surgical instrument detection and cropping
- Multi‑modal embedding comparison (image + text) for medical scenes
- Contrastive learning to optimize inter‑class and intra‑class feature distances

## Datasets
- Public: [CATARACTS](https://ieee-dataport.org/open-access/cataracts) 

## License
For academic research and educational use only.
