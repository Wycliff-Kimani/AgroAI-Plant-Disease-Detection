AgroAI - Plant Disease Detection

This repository contains a deep learning model developed using PyTorch and the ResNet18 architecture. The model is trained to classify plant leaf images and detect diseases in three crops: tomato, potato, and bell pepper. It was developed as part of the AgroAI mobile application project.

Project Description

The goal of this project is to help farmers and agricultural specialists diagnose plant diseases using AI-powered image classification. By uploading or capturing an image of a leaf, the application predicts the likely disease affecting the plant. The system is designed to support field-level diagnosis with minimal resources.

Model Overview

- Architecture: ResNet18 (pretrained on ImageNet)
- Framework: PyTorch
- Dataset: Subset of the PlantVillage dataset from Kaggle
- Number of classes: 15 (including healthy and diseased classes)
- Trained for 5 epochs using CPU
- Final model accuracy: approximately 85%

Dataset

The training data was sourced from the PlantVillage dataset. This version includes labeled images for three crops:

- Bell Pepper
- Potato
- Tomato

Each class folder contains images representing either a specific disease or healthy condition. The dataset was split into training and validation sets before training.

Model File

The trained model file (`AgroAImodel.pth`) is available at the following link:

[Download AgroAImodel.pth](https://drive.google.com/file/d/1F0qp7yHW8zhfNteUkjfEawPX5hgUXqiL/view?usp=sharing)

Classification Report

A full classification report (in JSON format) detailing precision, recall, and F1-score for each class is included in this repository as `AgroAI_classification_report.json`.

Intended Application

The model is intended to be integrated into the AgroAI mobile application, where it will be used to:

- Allow users to upload or take leaf images
- Run inference on-device or via API
- Display disease prediction results and possible recommendations

Future Work

- Retrain the model using the full PlantVillage dataset (all 14 crops) - ANd more locally collected images  dataset
- Improve model generalization through augmentation and fine-tuning
- Convert the model for mobile deployment (e.g., TorchScript or ONNX)
- Wrap model in an API for production use

License

This project is licensed under the MIT License.
