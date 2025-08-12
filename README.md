# Physics-Informed CNN for Astronomical Object Classification

## Overview
This project implements a convolutional neural network (CNN) for classifying astronomical objects, integrating physics-based constraints into the output layer to improve interpretability.

## Motivation
Fast and accurate classification of astronomical images can aid in identifying strong gravitational lenses and detecting features relevant to dark matter research.

## Dataset

### Lens Finding (Binary Classification)
Dataset Structure
The dataset should be organized into binary class folders (lenses and nonlenses) inside separate train and test directories.
```
dataset/
    train/
        lenses/
            file1.npy
            file2.npy
            ...
        nonlenses/
            file1.npy
            file2.npy
            ...
    test/
        lenses/
            file1.npy
            file2.npy
            ...
        nonlenses/
            file1.npy
            file2.npy
            ...
```
- Each .npy file contains a single image as a NumPy array.
- Images are normalized to [0, 1] during preprocessing.
- This dataset is for binary classification (lenses vs. nonlenses).

### Multi-Class Classification
The dataset used in this project contains labeled astronomical object images for multi-class classification.
If you wish to replicate the results:
- Use any public astronomical image dataset with similar categories (e.g., Sloan Digital Sky Survey data).
- Ensure the folder structure follows:
```  
dataset/
  train/
    class_0/
    class_1/
    class_2/
  val/
    class_0/
    class_1/
    class_2/
```

## Methods
- Framework: TensorFlow/Keras
- Physics-informed output layer to enforce astrophysical constraints
- Dataset: Telescope image dataset (preprocessed and normalized)
- Evaluation: Accuracy, ROC-AUC

## Results

### Gravitational Lensing Detection

The binary classification model for detecting gravitational lenses achieved high accuracy and strong discriminative performance. The ROC curve below shows the trade-off between True Positive Rate and False Positive Rate.

Test Accuracy: 98.39%

Test Loss: 0.0581

AUC: 0.9336

A high AUC score (>0.9) demonstrates strong discriminative ability, meaning the model effectively separates lens images from non-lens images.

<img width="827" height="556" alt="image" src="https://github.com/user-attachments/assets/6f5b53d4-0d66-4164-9f84-01e12955cbfc" />


### Multiclass Classification

Below is the baseline performance of the multi-class classification model on the initial dataset version. The ROC curves show the ability of the model to distinguish between the three astronomical object categories.


Notes:

- These results are from an initial run without extensive hyperparameter tuning or advanced preprocessing.

- They serve as a starting point for further improvements in model architecture, data augmentation, and dataset quality.

- Future work aims to significantly improve accuracy and AUC through iterative experimentation.

- <img width="825" height="562" alt="image" src="https://github.com/user-attachments/assets/e4751813-bddc-45e6-91bb-1320c6598506" />


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
