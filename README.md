# Brain-Tumor-Detection-Model

# Project Overview

The goal is to build a system that helps medical professionals in identifying the different types of brain tumors by just looking at the MRI image.

# Dataset

The project uses the Brain Tumor MRI dataset from Kaggle.
source: https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset
Classes:
1) glioma
2) meningioma
3) pituitary
4) notumor
The dataset is split into Training and Testing directories.

# Prerequisites

Google Account: To access Google colab
Kaggle Account: To download the dataset via API.
kaggle.json File: Your personal API token.

# Setup and Installation
1) Get your Kaggle API Token

a) Login to Kaggle.com
b) Go to settings
c) Scroll down to the API section.
d) Click "Create New API Token".
e) This will download a file (Kaggle.json)

2) Running the Project

a) Open the provided python script in Google Colab and run the cell
b) When prompted, click "choose files" and upload the kaggle.json file downloaded earlier.
c) This will automatically download the dataset, unzip and organise the files.

# Models & Techniques

Transfer Learning:
1) Base Model: MobileNetV2 (pre-trained on ImageNet).
2) Technique: We "freeze" the learned features of MobileNetV2 and add a custom classification head for our 4    tumor classes.
3) Features:
   1) Early Stopping: Stops training if the model stops improving to prevent overfitting.
   2) Model Checkpointing: Automatically saves the best version of the model during training.
   3) Learning Rate Scheduler: Adjusts learning speed dynamically.
   4) Performance: Typically achieves 90-98% accuracy.
