# Physics-Informed CNN for Astronomical Object Classification

## Overview
This project implements a convolutional neural network (CNN) for classifying astronomical objects, integrating physics-based constraints into the output layer to improve interpretability.

## Motivation
Fast and accurate classification of astronomical images can aid in identifying strong gravitational lenses and detecting features relevant to dark matter research.

## Dataset
The dataset used in this project contains labeled astronomical object images for multi-class classification.
Due to licensing and storage constraints, the dataset is not included in this repository.
If you wish to replicate the results:
- Use any public astronomical image dataset with similar categories (e.g., Sloan Digital Sky Survey data).
- Ensure the folder structure follows:
  
dataset/
  train/
    class_1/
    class_2/
    ...
  val/
    class_1/
    class_2/
    ...


## Methods
- Framework: TensorFlow/Keras
- Physics-informed output layer to enforce astrophysical constraints
- Dataset: Telescope image dataset (preprocessed and normalized)
- Evaluation: Accuracy, ROC-AUC

## Results
- ROC-AUC: [value]
- Accuracy: [value]
- [Add sample image or diagram]

## How to Run

pip install -r requirements.txt
python train.py


## Repository Structure

```
.
├── notebooks/                          # Main project notebooks
│   ├── lens_finding_physics_guided_cnn.ipynb        # Physics-informed CNN model, training, and results
│   └── astro_multiclass_classification_cnn.ipynb    # Multi-class classification of astronomical objects
│                        
│
├── requirements.txt                    # Python dependencies
└── README.md                           # Project documentation
```
