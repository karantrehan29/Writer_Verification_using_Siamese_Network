# LightSiameResNet: a nimble solution for writer verification with ResNet and Laplacian embeddings

A deep learning project implementing a siamese network with ResNet50 and Laplacian filtering for image pair analysis.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Prerequisites](#prerequisites)
4. [Installation](#installation)
5. [Setup](#setup)
6. [Usage](#usage)
7. [Contributing](#contributing)
8. [License](#license)

## Project Overview

This project implements a siamese neural network that combines ResNet50 with Laplacian edge detection to analyze pairs of images. The model is designed for tasks where comparing two images is necessary, such as verifying authenticity or detecting duplicates.

## Features

- **ResNet50 Backbone**: Leverages the pre-trained ResNet50 model for feature extraction.
- **Laplacian Filtering**: Enhances edge detection to capture detailed image features.
- **Siamese Network Architecture**: Processes image pairs to learn embeddings for comparison.
- **Optimized Training**: Implements callbacks for early stopping, model checkpointing, and learning rate adjustment.
- **Performance Analysis**: Evaluates model performance across different thresholds and exports results to Excel.

## Prerequisites

- **Python 3.8+**: Ensure Python is installed with the necessary package manager (pip).
- **TensorFlow 2.x**: For building and training the model.
- **Keras**: Included with TensorFlow for high-level model building.
- **OpenCV**: For image processing and Laplacian filtering.
- **Google Colab or Jupyter Notebook**: Recommended for running the code.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/karantrehan29/Writer_Verification_using_Siamese_Network.git
   cd Writer_Verification_using_Siamese_Network
2. Install dependencies as mentioned in Prerequisites.

## Setup

1. Mount Google Drive:

    Run the code in Google Colab and follow the prompts to mount your Google Drive.
    Ensure the IAM dataset is placed in the following structure:
    - /content/drive/MyDrive/IAM_Writer_lines/
    - /content/drive/MyDrive/IAM_Writers_lines_Validation/
    - /content/drive/MyDrive/IAM_Writer_lines_test/

## Usage

1. Training the Model:
    Execute the training script to build and train the model using the training and validation datasets.
    The model automatically saves checkpoints based on validation accuracy.

2. Model Evaluation:
    After training, the model evaluates performance on the test set across different thresholds (0.1 to 0.9).
    Results are saved in <filename>.xlsx, including accuracy, precision, recall, and F1 score.

3. Inference:
    Load the saved model to perform predictions on new image pairs.

