
# Lung Tumor Segmentation Using U-Net

This repository contains the implementation of a U-Net-based deep learning model for lung tumor segmentation in medical images (CT scans). The project is part of a larger effort to improve the detection and analysis of lung cancer using medical imaging and deep learning.

## Features

-   **U-Net Architecture**: A fully convolutional neural network designed for biomedical image segmentation.
-   **Dataset Handling**: Preprocessing and augmentation pipelines for medical images in DICOM or NIfTI format.
-   **Training and Evaluation**: Scripts for training the model and evaluating its performance.

## Table of Contents

1.  [Installation](#installation)
2.  [Dataset](#dataset)
3.  [Usage](#usage)

## Installation

1.  Clone this repository:

    ```
    git clone https://github.com/minhquang1802/CO3057-Extended-Topic-CV.git
    cd CO3057-Extended-Topic-CV
    ```

2.  Create a virtual environment and install dependencies:
	```
    python -m venv venv
    source venv/bin/activate  	# Linux/MacOS
    venv\Scripts\activate     	# Windows
    pip install -r requirements.txt
	```
## Dataset

The dataset can be access from [Medical Segmentation Decathlon](http://medicaldecathlon.com/).
The dataset consists of CT scans and their corresponding tumor masks.

-   Format: NIfTI (.nii.gz) files.
-   Ensure your dataset structure matches the following:
	```
    dataset/
    ├── imagesTr/         # Training images
    ├── imagesTs/         # Test images
    ├── labelsTr/         # Ground truth masks
    └── dataset.json      # Metadata file (optional)
    ```
### Dataset Preprocessing
Use the `preprocess.py` script to normalize, resize, and augment the dataset.

## Usage

### Training the Model

To train the U-Net model: `python train.py`
Learning rate, epoch, and other parameters can be change in this file.

## Acknowledgments

-   [Original U-Net Paper](https://arxiv.org/abs/1505.04597)
-   Lung tumor datasets: [http://medicaldecathlon.com/]
