# DeNoising the Images Using AutoEncoders

This project demonstrates how to use AutoEncoders to remove noise from images, achieving an impressive accuracy of **95.2%**. The model is trained on noisy image datasets and successfully reconstructs the original clean images.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Training the Model](#training-the-model)
- [Results](#results)


## Project Overview

The goal of this project is to reduce noise in images using an AutoEncoder model. The AutoEncoder learns to reconstruct clean images from noisy inputs. The dataset used contains clean images as the target, while the noisy versions are used as inputs. This project achieves a **95.2%** accuracy in restoring clean images.

### Key Features:
- **AutoEncoder**: Symmetrical encoder-decoder architecture.
- **Denoising**: Removes Gaussian noise added to the input images.
- **Accuracy**: Achieved a high accuracy of 95.2%.

## Dataset

The dataset consists of two sets of images:
1. **Clean Images**: Ground truth images without noise.
2. **Noisy Images**: Images with added Gaussian noise.

You can download the dataset from the appropriate source or generate your own noisy images using the provided scripts.

## Model Architecture

The AutoEncoder consists of:
- **Encoder**: A stack of convolutional layers that downsample the image into a compressed latent representation.
- **Latent Space**: A compact, lower-dimensional feature map representing the input.
- **Decoder**: A stack of transposed convolutional layers that upsample the latent representation back into the original image dimensions.

### Loss Function:
The model uses **Mean Squared Error (MSE)** to calculate the difference between the reconstructed image and the ground truth.

### Optimizer:
The model is trained using the **Adam Optimizer** with a learning rate of 0.001.

## Installation

To run this project locally, follow these steps:

### Prerequisites:
- Python 3.8 or higher
- TensorFlow
- NumPy
- Matplotlib
- OpenCV (for image processing)
