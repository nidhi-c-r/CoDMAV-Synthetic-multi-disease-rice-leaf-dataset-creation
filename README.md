# Lesion-Level Synthetic Generation for Co-existing Rice Leaf Disease Recognition

A dataset creation project focused on generating rice leaf images containing two co-existing diseases using lesion extraction, copy-paste augmentation, and image blending techniques.

## 📌 Project Overview

Most publicly available rice leaf disease datasets contain images of leaves affected by a single disease. This limits the availability of data for studying and recognizing multiple diseases occurring on the same leaf.

This project addresses this gap by creating a multi-disease rice leaf image dataset using lesions extracted from leaves affected by individual diseases. The extracted lesions are transferred onto other diseased leaves and blended to create images containing two co-existing diseases.

The project focuses on **dataset creation and evaluation**, supporting research into multi-disease rice leaf recognition.

## 🎯 Objectives

- Create rice leaf images containing two co-existing diseases.
- Extract and transfer disease lesions while preserving their visual characteristics.
- Improve the visual integration of transferred lesions using image blending techniques.
- Evaluate the quality of generated images using image quality metrics.
- Assess the usefulness of the generated dataset for multi-label disease recognition.

## 🌿 Diseases Covered

The project considers three rice leaf diseases:

- **Bacterial Leaf Blight (BLB)**
- **Rice Blast**
- **Brown Spot**

### Generated Disease Combinations

| Combination | Diseases |
|---|---|
| Combination 1 | BLB + Blast |
| Combination 2 | BLB + Brown Spot |
| Combination 3 | Blast + Brown Spot |

## ⚙️ Methodology

The project follows a multi-stage image processing pipeline.

### 1. Data Collection and Preprocessing
Rice leaf images are collected and organized according to disease category. The images are cleaned and preprocessed to prepare them for lesion extraction and dataset generation.

### 2. Lesion Segmentation and Extraction
The Segment Anything Model (SAM) is used to identify and extract disease lesions from rice leaf images.

### 3. Copy-Paste Augmentation
Extracted lesions are transferred between suitable rice leaf images to create samples containing two different diseases.

### 4. Image Blending
Feathered alpha compositing and multi-band Laplacian pyramid blending are used to integrate transferred lesions more naturally into the target images.

### 5. Dataset Augmentation
The generated images are augmented to create a more balanced dataset across the three disease combinations.

### 6. Quality Assessment and Model Evaluation
Image quality metrics are used to assess the generated images. Machine learning and deep learning models are evaluated to study their ability to recognize co-existing rice leaf diseases.

## 📊 Dataset Outcome

The final augmented dataset contains **2,700 images** across three disease combinations.

| Disease Combination | Number of Images |
|---|---:|
| BLB + Blast | 900 |
| BLB + Brown Spot | 900 |
| Blast + Brown Spot | 900 |
| **Total** | **2,700** |

The dataset is intended to support research on rice leaf images containing two co-existing diseases.

## 📈 Image Quality Assessment

The generated dataset was evaluated using the following image quality metrics.

| Metric | Value |
|---|---:|
| PSNR | 39.92 |
| SSIM | 0.965 |
| NIQE | 7.036 |
| BRISQUE | 45.471 |
| FID | 47.756 |

These metrics provide different perspectives on image similarity, structural consistency, perceptual quality, and distribution-level differences. They should be interpreted according to the properties and limitations of each metric.

## 🤖 Model Evaluation

The project evaluates multiple approaches for recognizing co-existing rice leaf diseases:

- Support Vector Machine (SVM)
- EfficientNet-B4
- Vision Transformer (ViT-Base/16)
- Swin Transformer

### Best Reported Results

The Swin Transformer achieved the following results:

| Evaluation Metric | Score |
|---|---:|
| Accuracy | 88.41% |
| Precision | 94.79% |
| Recall | 93.34% |
| F1-score | 94.06% |

These results indicate the potential of the generated dataset for multi-disease rice leaf recognition. Performance should also be validated on independent real-world images to assess generalization.

## 🛠️ Technologies and Techniques

**Tools and libraries**
- Python
- OpenCV
- NumPy
- Pandas
- PyTorch

**Image processing and dataset generation**
- Image cleaning and preprocessing
- SAM-based lesion segmentation and extraction
- Copy-paste augmentation
- Feathered alpha compositing
- Multi-band Laplacian pyramid blending
- Image augmentation

**Evaluation**
- PSNR
- SSIM
- NIQE
- BRISQUE
- FID
- Machine learning and deep learning model evaluation

## 🌾 Applications

- Research on multi-disease rice leaf recognition.
- Development and evaluation of agricultural image analysis systems.
- Dataset development for multi-label plant disease recognition.
- Research into lesion-level image augmentation and blending.
- Support for future automated rice leaf disease detection systems.

## 🔮 Future Work

- Extend the dataset to include rice leaves affected by all three diseases simultaneously.
- Include more real-world and field-collected rice leaf images.
- Improve lesion placement and blending to enhance visual realism.
- Validate the generated images with agricultural experts.
- Evaluate models on larger, independent datasets.
- Explore advanced multi-label learning approaches for improved disease recognition.

## 📂 Repository Contents

This repository contains the project materials and dataset resources associated with the creation of multi-disease rice leaf images.

Refer to the folders and files in the repository for the available datasets, implementation code, documentation, and project report.

## 👩‍💻 Project Team

**Project Guide**
- Prof. Swetha Patil — PES University

**Team Members**
- Nidhi C R
- Jayashree D

## 🔗 Project Repository

[CoDMAV — Synthetic Multi-Disease Rice Leaf Dataset Creation](https://github.com/nidhi-c-r/CoDMAV-Synthetic-multi-disease-rice-leaf-dataset-creation)

## 📄 Project Scope

This project focuses on creating and evaluating a dataset of rice leaf images containing two co-existing diseases. The generated images are intended for research and experimentation and should not be treated as a replacement for independently collected, expert-verified field data.
