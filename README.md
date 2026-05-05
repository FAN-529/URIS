# Siamese Network-based Intraoperative Video Analysis for Cataract Surgical Instrument Recognition
Undergraduate Research and Innovation Scheme (URIS) | The Hong Kong Polytechnic University

## Project Overview
This project focuses on **intraoperative surgical instrument recognition for cataract surgery** based on Siamese Network. By integrating YOLOv10 for real‑time instrument extraction and advanced multi‑modal embedding models, it solves the problems of background interference, similar‑instrument misclassification and information redundancy in traditional frame‑by‑frame detection, and significantly improves recognition accuracy and generalization.

This code library fully implements the TTT-UNet model, which integrates Test-Time Training (TTT) layers into the conventional U-Net architecture to resolve the core limitations in biomedical image segmentation: the inability of CNNs to effectively capture long-range dependencies and the excessively high computational cost of Transformers [1].

## Core Features
- The implementation preserves the symmetric encoder-decoder structure of the original U-Net and embeds custom TTT building blocks into the encoder. It transforms the traditional fixed hidden state into a trainable model and dynamically adjusts model parameters during the testing phase through self-supervised learning, achieving a balance between precise local feature extraction and effective long-range dependency modeling.
- The TTT building blocks in the code first process input features via cascaded residual blocks, instance normalization, and Leaky ReLU activation. They then generate multi-view Q, K, V features through parallel linear projection branches, which are sent to the TTT layer for self-supervised optimization. The refined features are fused and forwarded to the decoder for high-quality segmentation map reconstruction.
- The code library supports two official variants of TTT-UNet: TTT-UNet_Bot, which applies TTT layers only at the bottleneck of the network, and TTT-UNet_Enc, which integrates TTT layers across the entire encoder for full-range adaptive learning.

## Datasets
- Public: [CATARACTS](https://ieee-dataport.org/open-access/cataracts)

## Reference
- [1]R. Zhou et al., “TTT-Unet: Enhancing U-Net with Test-Time Training Layers for Biomedical Image Segmentation,” Sept. 2024, doi: 10.48550/arxiv.2409.11299

## License
For academic research and educational use only.
