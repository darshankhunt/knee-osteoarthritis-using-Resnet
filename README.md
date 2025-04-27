# Knee Osteoarthritis KL Grade Classification with ResNet18

This project applies deep learning (ResNet18) to classify knee X-ray images into Kellgren-Lawrence (KL) grades (0–4), a standard for assessing osteoarthritis severity. The pipeline includes data preprocessing, augmentation, class imbalance handling, model training/validation.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Results](#results)
- [Project Structure](#project-structure)

---

## Overview

- **Task:** Classify knee X-rays into KL grades (0–4).
- **Model:** ResNet18 (PyTorch, pretrained on ImageNet, final layer for 5 classes).
- **Techniques:** Data augmentation, class weighting for imbalance, stratified splits.
- **Visualization:** Confusion matrix.

---

## Features

- Custom PyTorch dataset loader
- Strong data augmentation (crop, rotate, color jitter, blur)
- Class weighting for imbalanced data
- Per-epoch training \& validation metrics
- Learning curve plots

---

## Installation

1. **Clone the repository:**

```bash
git clone https://github.com/darshankhunt/knee-osteoarthritis-using-Resnet.git
cd knee-osteoarthritis-using-Resnet
```

2. **Create and activate a virtual environment:**

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies:**

```bash
pip install -r requirements.txt
```


---

## Usage

1. **Prepare the dataset:**
    - Place images in `KLGrade_dataset/` with subfolders `0`, `1`, `2`, `3`, `4` (one for each KL grade).
2. **Run the notebook:**
    - Open `main.ipynb` in VS Code or Jupyter Notebook.
    - Execute cells step by step to preprocess data, train the model, and visualize results.
3. **Training:**
    - The notebook will split data, apply augmentations, train the model.
4. **Evaluation:**
    - After training, use the test set for final evaluation and confusion matrix.

---

## Dataset

- **Directory:** `KLGrade_dataset/`
- **Structure:**

```
KLGrade_dataset/
  ├── 0/
  ├── 1/
  ├── 2/
  ├── 3/
  └── 4/
```
Note: Dataset is not provided in this repo. Please use your own or request access if available.


---

## Results

### Learning Curves

- **Training accuracy:** ~86%
- **Validation accuracy:** ~84%

---

## Project Structure

```
knee-osteoarthritis-using-Resnet/
├── KLGrade_dataset/     
├── main.ipynb      
├── requirements.txt 
├── .gitignore   
└── README.md
```
