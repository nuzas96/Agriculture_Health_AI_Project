# Agriculture Health AI Project

Course: ISB46703 Principle of Artificial Intelligence

Domain: Agriculture Health

Project task: Plant leaf disease image classification

## Team Role Covered Here

Data Engineer: data preparation

- Collect data using a web crawler
- Filter and clean irrelevant images
- Standardize images into a consistent format
- Split the final dataset into training, validation, and testing sets
- Verify the final dataset before model training

## Selected Classes

The final dataset uses 5 classes:

1. yellow_leaf_disease
2. leaf_rust
3. powdery_mildew
4. leaf_spot
5. leaf_blight

## Final Clean Dataset

The original target was up to 10,000 images. After manual filtering, exact duplicate removal, visual review, and class balancing, the final cleaned dataset contains 5,750 images. This is valid because it is above the 3,000 minimum and stays below the 10,000 maximum.

All final images are RGB JPG images resized to 224 x 224 pixels.

The image dataset is stored in Google Drive because it is too large for GitHub:

https://drive.google.com/drive/folders/1vekKwpUeoxEUURKpIukM656538snPFR8?usp=sharing

| Class               |     Train | Validation |      Test |     Total |
| ------------------- | --------: | ---------: | --------: | --------: |
| yellow_leaf_disease |       812 |        164 |       174 |     1,150 |
| leaf_rust           |       812 |        164 |       174 |     1,150 |
| powdery_mildew      |       812 |        164 |       174 |     1,150 |
| leaf_spot           |       812 |        164 |       174 |     1,150 |
| leaf_blight         |       812 |        164 |       174 |     1,150 |
| **Total**           | **4,060** |    **820** |   **870** | **5,750** |

Final technical check:

- The final dataset folders were checked after manual filtering.
- Exact duplicate images were removed.
- All classes were balanced to 1,150 images each.
- Remaining images are organized into train, validation, and test folders.
- Image relevance was checked manually, so a small number of imperfect images may still exist.

## How to Run the Data Engineering Notebook

Open Anaconda Prompt or PowerShell:

```powershell
conda activate ISB46703
jupyter notebook
```

Open:

```text
notebooks/01_data_engineering_agriculture_health.ipynb
```

Run the notebook step by step. The notebook is the main Data Engineer workflow for this project.

## Folder Structure

```text
Agriculture_Health_AI_Project/
  README.md
  notebooks/
    01_data_engineering_agriculture_health.ipynb
  reports/
    data_engineering_final_report.csv
  data/
    README.md
```
