# Deep-Lesion-Scan: A Soft Attention-Enhanced ResNet Model for Multi-Class Dermoscopic Image Diagnosis

## Overview
This repository contains the implementation of a deep learning model designed to classify skin lesions from dermoscopic images. The model enhances the ResNet50 architecture with a lightweight Soft Attention mechanism to dynamically focus on diagnostically crucial regions, improving classification accuracy and interpretability. The project uses the HAM10000 dataset and addresses challenges such as class imbalance and model transparency.

## Key Features
- **Soft Attention Mechanism**: Enhances ResNet50 by focusing on clinically significant regions in dermoscopic images.
- **Class Imbalance Mitigation**: Utilizes oversampling and weighted loss functions to handle imbalanced data.
- **High Performance**: Achieves a test accuracy of 92.6% and a weighted ROC-AUC of 0.985.
- **Interpretability**: Generates attention heatmaps and Grad-CAM visualizations to explain model predictions.

## Dataset
The model is trained on the [HAM10000 dataset](https://doi.org/10.1038/sdata.2018.161), which consists of 10,015 dermoscopic images across 7 classes:
- Melanocytic nevi (NV)
- Melanoma (MEL)
- Benign keratosis (BKL)
- Basal cell carcinoma (BCC)
- Actinic keratoses (AKIEC)
- Vascular lesions (VASC)
- Dermatofibroma (DF)


## Results
The model achieves the following performance metrics:

| Metric           | Baseline Model | Attention Model |
|------------------|---------------|-----------------|
| Accuracy         | 0.85          | 0.926           |
| Precision (macro)| 0.81          | 0.88            |
| Recall (macro)   | 0.80          | 0.87            |
| F1-Score (macro) | 0.82          | 0.89            |
| ROC AUC (macro)  | 0.91          | 0.982           |

## Visualizations
- **Attention Heatmaps**: Highlight diagnostically relevant regions in the input images.
- **Grad-CAM**: Visualizes the model's focus areas during prediction.

Example visualizations can be found in the `results/` directory.


