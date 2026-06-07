# Data Analyst

This folder contains the Data Analyst part for the Agriculture Health AI Project.

## Role

The Data Analyst is responsible for analyzing and visualizing the dataset and model performance. This includes dataset class distribution, dataset split distribution, model performance comparison, training accuracy/loss visualization, hyperparameter tuning visualization, confusion matrix evaluation, and final model conclusion.

## Folder Contents

| Folder | Description |
|---|---|
| notebooks | Contains the Data Analyst Jupyter Notebook used for analysis and visualization. |
| visualizations | Contains all generated graph images and confusion matrix outputs. |
| reports | Contains the Data Analyst summary report. |

## Main Analysis

The Data Analyst notebook includes:

- Dataset class distribution
- Dataset split distribution
- Training and validation accuracy/loss graphs
- Model accuracy comparison
- mAP comparison
- Training time comparison
- Parameter comparison
- Hyperparameter tuning result visualization
- Confusion matrix evaluation
- Final model conclusion

## Models Compared

The models evaluated in this project are:

1. ResNet50
2. DenseNet121
3. MobileNetV3Small

## Final Conclusion

Based on the evaluation results, ResNet50 is the best model for this Agriculture Health classification task because it achieved the highest test accuracy and mAP. The confusion matrix evaluation also supports this result. However, MobileNetV3Small can be considered if speed and lightweight deployment are more important.
