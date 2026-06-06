# Data Scientist - Model Training

This folder contains the Data Scientist part for the Agriculture Health AI Project.

## Role
The Data Scientist role focuses on data modelling using CNN transfer learning.

## Models Used
- MobileNetV3Small
- ResNet50
- DenseNet121

## Training Setup
- Dataset: Agriculture Health plant disease image dataset
- Number of classes: 5
- Image size: 224 x 224
- Epochs: 50 for each model
- Evaluation metrics: Test Accuracy, mAP, Training Time, and Total Parameters

## Final Result

| Model | Test Accuracy (%) | mAP (%) | Training Time (minutes) | Total Parameters |
|---|---:|---:|---:|---:|
| ResNet50 | 71.15 | 78.56 | 98.01 | 23,597,957 |
| DenseNet121 | 63.56 | 70.58 | 99.81 | 7,042,629 |
| MobileNetV3Small | 62.64 | 68.99 | 8.20 | 942,005 |

## Conclusion
ResNet50 achieved the best performance with the highest test accuracy and mAP. MobileNetV3Small was the fastest and lightest model.
