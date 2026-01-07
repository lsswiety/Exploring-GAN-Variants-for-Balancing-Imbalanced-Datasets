# Exploring GAN Variants for Balancing Imbalanced Datasets

**Course:** Special Topics in Artificial Intelligence – Section 1, Spring 2024/2025  
**Student:** Laya Swiety  
**Instructor:** Dr. Yousef Sanjalawe  

---

## **Project Overview**

This project demonstrates how **Generative Adversarial Networks (GANs)** can be used to **balance imbalanced datasets**.  

We implemented two GAN variants:

1. **Vanilla GAN**  
2. **DCGAN (Deep Convolutional GAN)**

A **CNN classifier** is trained on:

- Original imbalanced dataset  
- Vanilla GAN balanced dataset  
- DCGAN balanced dataset  

Metrics like **accuracy, F1-score, recall, and confusion matrices** are used to evaluate performance.

---

## **Project Code Structure**

The main Colab notebook contains the following steps:

1. **Dataset Preparation**
   - Load MNIST dataset  
   - Artificially create imbalanced dataset (digit 0 as minority)  
   - Prepare training/testing sets for CNN  

2. **Vanilla GAN**
   - Define Generator and Discriminator  
   - Train on minority class  
   - Generate synthetic samples for balancing  

3. **DCGAN**
   - Define simplified DCGAN Generator and Discriminator  
   - Train on minority class  
   - Generate synthetic samples for balancing  

4. **Classifier (CNN)**
   - Train CNN on:
     - Original imbalanced data  
     - Vanilla GAN balanced data  
     - DCGAN balanced data  
   - Evaluate with confusion matrix, classification report, and performance table  

5. **Visualization**
   - Sample generated images from Vanilla GAN and DCGAN  
   - Performance comparison table & plots  
