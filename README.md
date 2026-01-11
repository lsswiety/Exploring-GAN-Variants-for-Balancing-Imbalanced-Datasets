# Exploring GAN Variants for Balancing Imbalanced Datasets

**Course:** Special Topics in Artificial Intelligence (Spring 2024/2025)
**Student Name:** [Your Name Here]
**University:** KASIT, University of Jordan

## Project Overview
This project addresses the challenge of imbalanced datasets in machine learning by using Generative Adversarial Networks (GANs) to generate synthetic data for the minority class.

The study implements and compares two GAN architectures:
1. Vanilla GAN: A baseline generative model using fully connected layers.
2. DCGAN (Deep Convolutional GAN): An advanced variant using convolutional layers for better feature capture.

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
| Original Imbalanced | [Insert Score] | [Insert Score] |
| Balanced (Vanilla GAN) | [Insert Score] | [Insert Score] |
| Balanced (DCGAN) | [Insert Score] | [Insert Score] |

Observation: Balancing the dataset with GAN-generated samples generally improves the classifier's ability to correctly identify the minority class. DCGAN often provides higher quality synthetic samples compared to the Vanilla GAN, leading to better classification performance.

## How to Run
1. Open the notebook `Project_GAN_Imbalance_Analysis.ipynb` in Google Colab.
2. Change the Runtime type to GPU (T4) for faster training.
3. Run the cells in the order presented (Steps 1 through 5).

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
