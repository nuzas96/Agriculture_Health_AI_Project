# Data Analyst Summary Report

## Project Topic

The topic of this project is Agriculture Health. The project focuses on classifying plant leaf diseases using image classification models.

## Data Analyst Role

The Data Analyst role is responsible for analyzing and visualizing the dataset and model performance. This includes understanding the class distribution, visualizing training performance, evaluating model results, displaying the confusion matrix, and drawing a final conclusion on the best model.

## Dataset Overview

The dataset contains 5 plant disease classes:

1. yellow_leaf_disease
2. leaf_rust
3. powdery_mildew
4. leaf_spot
5. leaf_blight

Each class contains 1,150 images, giving a total of 5,750 images.

## Dataset Split

The dataset is divided into three parts:

| Dataset Split | Number of Images |
|---|---:|
| Training | 4,060 |
| Validation | 820 |
| Testing | 870 |

The dataset is balanced because every class has the same number of images. This helps reduce bias during model training.

## Models Evaluated

Three CNN models were evaluated:

1. ResNet50
2. DenseNet121
3. MobileNetV3Small

## Model Performance Summary

| Model | Test Accuracy (%) | mAP (%) | Training Time (minutes) | Total Parameters |
|---|---:|---:|---:|---:|
| ResNet50 | 71.15 | 78.56 | 98.01 | 23,597,957 |
| DenseNet121 | 63.56 | 70.58 | 99.81 | 7,042,629 |
| MobileNetV3Small | 62.64 | 68.99 | 8.20 | 942,005 |

## Visualization and Evaluation

The Data Analyst notebook visualizes the dataset distribution and model performance using several graphs. These include class distribution, dataset split distribution, test accuracy comparison, mAP comparison, training time comparison, parameter comparison, training accuracy/loss graphs, hyperparameter tuning results, and confusion matrix evaluation.

The confusion matrix is used to evaluate how well each model classifies each plant disease class in the testing dataset. The values on the main diagonal represent correct predictions, while the values outside the diagonal represent incorrect predictions.

## Analysis

ResNet50 achieved the highest test accuracy and mAP among the three models. This shows that ResNet50 performed the best in classifying plant leaf diseases in this project.

DenseNet121 had lower accuracy compared to ResNet50, even though it required almost the same training time. MobileNetV3Small had the fastest training time and the lowest number of parameters, but its accuracy and mAP were lower than the other models.

Based on the confusion matrix, ResNet50 also shows stronger overall classification performance because more predictions are concentrated along the main diagonal. This supports the result that ResNet50 is the most suitable model when accuracy is the main priority.

## Final Conclusion

Based on the results, ResNet50 is the best model for this Agriculture Health classification task because it achieved the highest test accuracy and mAP. The confusion matrix evaluation also supports this conclusion because ResNet50 produced stronger classification performance compared to the other models.

However, ResNet50 requires more parameters and longer training time. MobileNetV3Small is the fastest and lightest model, but its accuracy and mAP are lower. Therefore, if accuracy is the main priority, ResNet50 is the most suitable model. If speed and lightweight deployment are more important, MobileNetV3Small can be considered.
