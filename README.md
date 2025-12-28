# Silkworm Disease Detection using Explainable Deep Learning

# Overview
This project implements an end-to-end deep learning pipeline for automatic silkworm disease detection from images with a strong focus on explainability and disease pattern analysis.

Unlike basic image classification projects, this work not only predicts whether a silkworm is Healthy or Diseased, but also:
- Explains why the model made a decision
- Highlights affected regions in the image
- Discovers hidden disease patterns using unsupervised learning
- 
# Project Description
This project focuses on automatic detection of silkworm diseases using deep learning–based image classification. Silkworm diseases can significantly affect silk production, and early detection is essential to reduce economic loss in sericulture farms. Manual inspection is time-consuming and error-prone, which motivates the need for an automated solution.
In this work, I designed an end-to-end deep learning pipeline that takes silkworm images as input, preprocesses them, and classifies them into healthy or diseased categories. The model learns visual disease patterns such as texture changes, discoloration, and irregular shapes from images.
The system was trained and evaluated using standard performance metrics including accuracy, precision, recall, F1-score, and confusion matrix. Experimental results show that the model is capable of distinguishing diseased silkworms with good reliability, demonstrating the feasibility of deep learning for real-world agricultural applications.
This project helped me gain hands-on experience in dataset handling, model training, performance evaluation, and result interpretation, and strengthened my understanding of how deep learning can be applied to real-life biological and agricultural problems.


# Problem Statement
Traditional silkworm disease identification:
- Requires expert knowledge  
- Is time-consuming  
- Is prone to human error  

This project aims to build an automated, interpretable, and reliable system that assists early disease detection using deep learning.

# Methodology

# 1️ Image Input
Silkworm images are resized and normalized before being passed to the model.

# 2️ Disease Classification
- A CNN-based EfficientNet-B0 model is used.
- The model classifies images into:
  - Healthy
  - Diseased
- A softmax confidence score is generated for reliability.


# 3️ Deep Feature Extraction
- High-level feature representations are extracted from the CNN backbone.
- These features capture disease-related textures and structural patterns.

# 4️ Disease Pattern Discovery (Unsupervised Learning)
To analyze diseased samples:
- PCA (Principal Component Analysis) reduces feature dimensionality.
- KMeans clustering groups similar disease patterns.
  
Each cluster represents a distinct disease manifestation, discovered without manual labels.

# 5️ Explainability using Grad-CAM
- Grad-CAM is applied to visualize regions influencing the model’s decision.
- Heatmaps highlight affected areas on the silkworm body.
- This improves transparency and trust in predictions.


# 6️ Disease Reasoning
Each discovered pattern is mapped to:
- A likely disease category
- A human-readable explanation

This bridges the gap between deep learning predictions and biological understanding.

# Key Learnings
- Understood the complete deep learning workflow from data preprocessing to evaluation
- Gained experience in image-based disease detection
- Learned how to analyze confusion matrix and F1-score instead of relying only on accuracy
- Improved skills in Python, PyTorch/TensorFlow, and GitHub project structuring

# Dataset Information

The dataset consists of healthy and diseased silkworm images collected from publicly available sources and curated datasets.

# Dataset Structure
dataset/
├── healthy/
│ ├── image1.jpg
│ ├── image2.jpg
├── diseased/
│ ├── image1.jpg
│ ├── image2.jpg



# Key Features
- Healthy vs Diseased classification
- Explainable AI using Grad-CAM
- Unsupervised disease pattern analysis
- Confidence-based predictions
- Visual and textual disease interpretation

#  Tech Stack
- Python  
- PyTorch  
- TIMM  
- OpenCV  
- Scikit-learn  
- Matplotlib  
- Pillow  


#  How to Run

# Install Dependencies
```bash
pip install -r requirements.txt
