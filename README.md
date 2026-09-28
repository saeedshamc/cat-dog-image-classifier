# Cat and Dog Image Classifier

A convolutional neural network built with TensorFlow and Keras that classifies images as cats or dogs. This project is part of the freeCodeCamp Machine Learning with Python certification.

## Overview

- Binary image classification (cat vs. dog)
- Training set: 2000 images, validation set: 1000 images, test set: 50 unlabeled images
- Data augmentation (rotation, shifts, shear, zoom, horizontal flip) to reduce overfitting
- CNN with four Conv2D + MaxPooling2D blocks, dropout, and a sigmoid output layer

## Model Architecture

| Layer | Details |
|-------|---------|
| Conv2D + MaxPooling2D | 32 filters, 3x3, ReLU |
| Conv2D + MaxPooling2D | 64 filters, 3x3, ReLU |
| Conv2D + MaxPooling2D | 128 filters, 3x3, ReLU |
| Conv2D + MaxPooling2D | 128 filters, 3x3, ReLU |
| Dropout | 0.3 |
| Flatten | |
| Dense | 512 units, ReLU |
| Dropout | 0.3 |
| Dense | 1 unit, sigmoid |

Optimizer: Adam. Loss: binary cross-entropy. Epochs: 30. Batch size: 128. Image size: 150x150.

## Results

The model reaches the freeCodeCamp requirement of at least 63% accuracy on the test images.

| Metric | Value |
|--------|-------|
| Test accuracy | 80% |
| Validation accuracy | 85% |

Add your training curves here:

![Training curves](images/training_curves.png)

## Getting Started

### Run in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/fcc_cat_dog_completed.ipynb)

### Run locally

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook fcc_cat_dog_completed.ipynb
```

On Windows, activate the environment with `venv\Scripts\activate`. The notebook downloads the dataset automatically, but the `!wget` and `!unzip` commands require a Unix shell. On Windows, use Colab or WSL.

## Project Structure

```
.
├── fcc_cat_dog_completed.ipynb
├── requirements.txt
├── README.md
├── .gitignore
└── images/
    └── training_curves.png
```

## Technologies

Python, TensorFlow, Keras, NumPy, Matplotlib

## Acknowledgments

Dataset and challenge by [freeCodeCamp](https://www.freecodecamp.org).
