# DeepWeeds Classification

Applied deep learning project for weed species classification using the DeepWeeds dataset, comparing a custom CNN baseline against transfer learning and fine-tuning methods.

## Project Overview
This repository contains the materials for a COMP6012 Applied Deep Learning assignment. The project focuses on image classification using the DeepWeeds dataset, with the goal of comparing a baseline convolutional neural network trained from scratch against transfer learning approaches based on a pretrained backbone.

The project is designed around fair experimentation, clear documentation, and reproducible results in Google Colab.

## Main Goal
To evaluate whether transfer learning improves weed-species classification performance on the DeepWeeds dataset compared with a baseline CNN trained from scratch.

## Planned Experiments
The project includes three main experimental settings:

1. **Baseline CNN**  
   A custom convolutional neural network trained from scratch.

2. **Transfer Learning with Frozen Backbone**  
   A pretrained ResNet-18 used as a fixed feature extractor, with only the classifier head trained.

3. **Fine-Tuned Transfer Learning**  
   The same pretrained ResNet-18, with upper layers unfrozen and fine-tuned using a smaller learning rate.

## Dataset
**Dataset:** DeepWeeds  
**Task:** Multi-class image classification  
**Domain:** Agricultural computer vision / weed species recognition

DeepWeeds was chosen because it is more unique than very common image classification datasets, is realistic and practical, and remains manageable for Google Colab experiments.

## Evaluation
The main evaluation metrics planned for this project are:
- accuracy
- macro precision
- macro recall
- macro F1-score
- confusion matrix

Additional analysis will include:
- training and validation curves
- misclassified examples
- discussion of model performance versus training cost