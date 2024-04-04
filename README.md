# Semantic Segmentation with Data Augmentation

## Overview

This project examines the impact of data augmentation on the performance of semantic segmentation models using the SHIFTDataset, focusing on autonomous driving tasks.

## Purpose

The goal is to assess how different data augmentation techniques affect model accuracy, generalization, and robustness, and to identify effective strategies for enhancing model performance.

## Dataset and Libraries

- **PyTorch & PyTorch Lightning**: Used for data handling and processing, these tools facilitate experimentation with the SHIFTDataset.
- **SHIFTDataset**: A synthetic driving dataset designed for autonomous driving tasks, with multi-view RGB cameras, depth cameras, LiDAR point clouds, and annotations for 23 classes.

## SHIFTDatasetWrapper

Developed to integrate data augmentation techniques into the training process, allowing for diverse transformations on images to improve model performance and reduce overfitting.

## Data Augmentation Techniques

### Mixing Images
- **Mixup**: Combines two images and their labels to improve generalizability.
- **Fade**: Blends two images horizontally or vertically to enhance robustness.
- **Advanced Blending**: Diagonal, Cross, and Grid techniques for diverse training examples.

### Mixing Ground Truth Images
- **Probability-Based Mixing**: Chooses class for each pixel based on class probabilities.
- **One Hot Encoding**: Uses tensor matrices to maintain class information for each pixel.

## Experimental Setup

- **Early Stopping & GPU Acceleration**: Used to optimize training time and computational efficiency.
- **Training/Test Split**: 90% of data for training, 10% for testing.
- **Batch Size & Epochs**: Set to balance computational efficiency and constraints, with a maximum of 20 epochs.

## Results

Data augmentation improved model performance, with Fade techniques showing better results than Mixup. Horizontal Fade techniques were more effective than vertical ones.

## Conclusion

Data augmentation is effective in enhancing semantic segmentation model performance, with certain techniques and application methods proving more beneficial than others.

### For more information about the techniques used, the results, ... , see the pdf report in the repo. 
