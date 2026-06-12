## Notebook Files

* `Data_Scientist_Model_Training.ipynb` is the main Data Scientist notebook. It contains dataset preparation, hyperparameter tuning, model training, evaluation, final comparison, saved model preparation, and prediction CSV generation.
* `Data_Scientist_Final_Clean.ipynb` is a simplified clean reference notebook used for easier viewing and explanation.


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

## Hyperparameter Tuning

A hyperparameter tuning experiment was conducted in the main training notebook before final model training. Three trials were tested for each CNN model by changing the learning rate, dropout value, and trainable layer setting.

| Trial   | Learning Rate | Dropout | Trainable Layers         |
| ------- | ------------: | ------: | ------------------------ |
| Trial 1 |         0.001 |     0.3 | Frozen base              |
| Trial 2 |        0.0001 |     0.4 | Frozen base              |
| Trial 3 |       0.00001 |     0.3 | Fine-tune last 10 layers |

Each trial was trained for 3 epochs using the training and validation datasets. The best trial was selected based on validation accuracy.

Selected hyperparameters:

| Model            | Selected Trial | Learning Rate | Dropout | Trainable Layers | Best Validation Accuracy (%) |
| ---------------- | -------------- | ------------: | ------: | ---------------- | ---------------------------: |
| DenseNet121      | Trial 1        |         0.001 |     0.3 | Frozen base      |                        58.29 |
| MobileNetV3Small | Trial 1        |         0.001 |     0.3 | Frozen base      |                        60.37 |
| ResNet50         | Trial 1        |         0.001 |     0.3 | Frozen base      |                        63.17 |

Since Trial 1 was selected for all three models, the final 50-epoch training used:

* Learning rate: 0.001
* Dropout: 0.3
* Trainable layers: Frozen base

The tuning results are saved in:

* `results/hyperparameter_tuning_results.csv`
* `results/selected_hyperparameters.csv`


## Final Result

| Model | Test Accuracy (%) | mAP (%) | Training Time (minutes) | Total Parameters |
|---|---:|---:|---:|---:|
| ResNet50 | 71.15 | 78.56 | 98.01 | 23,597,957 |
| DenseNet121 | 63.56 | 70.58 | 99.81 | 7,042,629 |
| MobileNetV3Small | 62.64 | 68.99 | 8.20 | 942,005 |

## Conclusion
ResNet50 achieved the best performance with the highest test accuracy and mAP. MobileNetV3Small was the fastest and lightest model.

## Saved Models

The trained model files are not uploaded directly to GitHub because the files are large. The saved models are stored in Google Drive.

Saved models included:
- mobilenetv3small_model.keras
- resnet50_model.keras
- densenet121_model.keras

Google Drive link:
[Saved Models ZIP](https://drive.google.com/file/d/1UV-klIND0hV5SWNfJySwhYp-njy__SHS/view?usp=sharing)
