# Exploring GAN Variants for Balancing Imbalanced Datasets

**Course:** Special Topics in Artificial Intelligence (Spring 2024/2025)
**Student Name:** [Your Name Here]
**University:** KASIT, University of Jordan

## Project Overview
This project addresses the challenge of imbalanced datasets in machine learning by using Generative Adversarial Networks (GANs) to generate synthetic data for the minority class.

The study implements and compares two GAN architectures:
1. **Vanilla GAN:** A baseline generative model using fully connected layers.
2. **DCGAN (Deep Convolutional GAN):** An advanced variant using convolutional layers for better feature capture.

We evaluate the impact of data augmentation by training a classifier on three dataset scenarios:
* Original Imbalanced Dataset (Baseline)
* Dataset Balanced with Vanilla GAN
* Dataset Balanced with DCGAN

## Dataset
* **Dataset Used:** MNIST (Handwritten Digits)
* **Imbalance Strategy:** We simulated a severe class imbalance by reducing the number of samples for Digit 0 to only 10% of its original size.

## Methodology

### 1. GAN Implementation
Both GANs were trained exclusively on the minority class (Digit 0) to learn its underlying distribution.
* **Vanilla GAN:** Generator and Discriminator built using standard Linear layers (MLP).
* **DCGAN:** Generator uses Transposed Convolutions to upsample noise; Discriminator uses Strided Convolutions for downsampling.

### 2. Data Augmentation
Synthetic samples were generated to equate the count of the minority class with the majority class, perfectly balancing the dataset.

### 3. Classification and Evaluation
A Multi-Layer Perceptron (MLP) classifier was trained on the three dataset variations. Performance was measured using:
* Accuracy
* F1-Score (Weighted)

## Results Summary

| Scenario | Accuracy | F1-Score |
| :--- | :--- | :--- |
| Original Imbalanced | 0.9612 | 0.9580 |
| Balanced (Vanilla GAN) | 0.9745 | 0.9720 |
| Balanced (DCGAN) | 0.9830 | 0.9815 |

**Observation:** Balancing the dataset with GAN-generated samples improved the classifier's ability to correctly identify the minority class. The DCGAN provided higher quality synthetic samples compared to the Vanilla GAN, leading to the best overall classification performance.

## Dependencies
* Python 3.x
* PyTorch
* Torchvision
* Matplotlib
* Seaborn
* Scikit-Learn
* Pandas
* Numpy

## License
This project is for academic purposes as part of the Special Topics in AI course.
