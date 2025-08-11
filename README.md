# Physics-Informed CNN for Astronomical Object Classification

## Overview
This project implements a convolutional neural network (CNN) for classifying astronomical objects, integrating physics-based constraints into the output layer to improve interpretability.

## Motivation
Fast and accurate classification of astronomical images can aid in identifying strong gravitational lenses and detecting features relevant to dark matter research.

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
│   ├── astro_multiclass_classification_cnn.ipynb    # Multi-class classification of astronomical objects
│   └── model_testing.ipynb                         # Additional evaluation / experiments
│
├── requirements.txt                    # Python dependencies
└── README.md                           # Project documentation
```
