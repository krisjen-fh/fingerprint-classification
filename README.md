<div align="center">
<h1>🚀 Fingerprint Real vs Altered Detection</h1>

<h3>Hybrid Feature Extraction using Gabor Filters and Convolutional Neural Networks</h3>

Reference: https://doi.org/10.1016/J.COMPELECENG.2021.107387
 </div>
 
## 📌 Overview
This project implements a hybrid feature extraction framework to analyze differences between real and altered fingerprint images (easy, medium, hard). The approach combines handcrafted texture descriptors (Gabor filters) and deep representations (CNN) to produce a fused feature dataset for further classification tasks.

## 🔄 Methodology
### 1️. Preprocessing

  Fingerprint images undergo
  - Grayscale conversion
  - Contrast enhancement using CLAHE
  - Morphological refinement (dilation, erosion, closing)

### 2. Gabor-Based Feature Extraction

Multi-orientation Gabor filters are applied to capture ridge texture characteristics.
Statistical descriptors (e.g., mean, standard deviation, entropy) are computed from filter responses, resulting in 72 handcrafted features per image.

Output:
  - Gabor_features_real.csv
  - Gabor_features_altered.csv

### 3. CNN-Based Feature Extraction

A custom Convolutional Neural Network (CNN) is implemented in PyTorch to extract deep spatial representations from fingerprint images.
Feature vectors are exported as:

  - CNN_features_real.csv
  - CNN_features_altered.csv

### 4. Feature Fusion

Handcrafted and deep features are merged using image filenames as identifiers.
Final fused datasets:

  - Fusion_features_real.csv
  - Fusion_features_altered.csv

## 🎯 Application

The resulting fused feature datasets are intended for:

  - Fingerprint alteration detection
  - Machine learning classification
  - Experimental research analysis

## 👥 Team Members
  - Muh. Fadhil
  - Sofia Zahira Rohman
  - Krisjen Fraulein Hutagalung
