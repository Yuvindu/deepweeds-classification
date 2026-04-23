

# Project Plan

## Project Title
DeepWeeds Image Classification Using CNNs and Transfer Learning

## Repository Goal
This repository contains all materials for the Applied Deep Learning assignment project, including planning notes, experiment records, notebooks, code, results, and final report assets.

## Problem Statement
This project investigates how well deep learning models can classify weed species from field images in the DeepWeeds dataset. The goal is to compare a custom CNN trained from scratch against transfer learning approaches based on a pretrained model, and determine whether transfer learning improves classification performance on a realistic agricultural vision task.

## Why This Project
This project is a good fit for the assignment because:
- it uses a realistic public dataset rather than a toy dataset
- it supports a clear image classification task that is easy to explain
- it allows a strong comparison between baseline and improved models
- it is practical to train and evaluate in Google Colab
- it creates opportunities for meaningful discussion through confusion matrices, misclassifications, and transfer learning analysis

## Dataset
**Dataset:** DeepWeeds  
**Task type:** Multi-class image classification  
**Domain:** Agricultural computer vision / weed species recognition

### Reasons for choosing DeepWeeds
- more unique than very common datasets such as pets or flowers
- realistic field images with natural background variation
- manageable dataset size for Colab experiments
- suitable for CNNs and transfer learning
- easy to justify in terms of practical real-world relevance

## Main Objective
To build and compare deep learning models for weed species classification, and evaluate whether transfer learning and fine-tuning outperform a baseline CNN trained from scratch.

## Research Question
How much does transfer learning improve weed-species classification performance on the DeepWeeds dataset compared with a baseline CNN trained from scratch?

## Planned Experimental Settings
The project will use three main experimental settings.

### Experiment 1: Baseline CNN
A custom convolutional neural network trained from scratch on the DeepWeeds dataset.

**Purpose:** Establish a baseline that is directly connected to core unit content.

### Experiment 2: Transfer Learning with Frozen Backbone
A pretrained ResNet-18 model used as a feature extractor, with the backbone frozen and only the classifier head trained.

**Purpose:** Measure the benefit of transfer learning over the baseline.

### Experiment 3: Fine-Tuned Transfer Learning
The same pretrained ResNet-18 model, but with upper layers unfrozen and fine-tuned using a smaller learning rate.

**Purpose:** Test whether partial fine-tuning gives further improvements beyond frozen transfer learning.

## Planned Evaluation Metrics
Primary and supporting metrics will be:
- accuracy
- macro precision
- macro recall
- macro F1-score
- confusion matrix

Additional analysis will include:
- training and validation loss curves
- training and validation accuracy curves
- examples of misclassified images
- comparison of training cost and model performance

## Initial Training Plan
The exact values may be adjusted after early experiments, but the initial plan is:
- image size: 224 x 224
- batch size: 32
- loss function: cross-entropy loss
- optimizer: Adam
- early stopping based on validation loss
- model checkpointing for best validation result
- data augmentation on training set only

## Planned Data Preparation
The following preprocessing steps are expected:
- resize images to a fixed resolution
- normalize image tensors
- create train, validation, and test splits
- apply training-only augmentation such as horizontal flips, small rotations, and random crops

## Fair Comparison Strategy
To keep comparisons fair:
- all models will use the same dataset split
- evaluation metrics will be consistent across experiments
- training conditions will be kept as similar as possible unless a change is part of the experimental design
- improvements will be described clearly relative to the baseline

## Expected Report Structure
The final report will follow the assignment structure:

### Part A: Problem Definition, Motivation, and Data
- define the problem
- explain motivation and relevance
- describe the dataset and preprocessing
- justify chosen metrics and baseline

### Part B: Methods, Models, and Implementation
- describe the baseline CNN
- describe the pretrained model setup
- explain what changes between each experiment
- document training setup and hyperparameters

### Part C: Experiments, Results, and Discussion
- compare the three experimental settings
- present tables, plots, and confusion matrices
- discuss what worked and what did not
- analyse limitations, failure cases, and future improvements

## Deliverables to Maintain in This Repository
- planning notes in markdown
- experiment logs
- Colab notebooks
- source code modules if needed
- saved figures and tables
- final report assets
- presentation notes

## Immediate Next Steps
1. confirm dataset loading method in Colab
2. inspect class labels and dataset structure
3. define the train, validation, and test split strategy
4. create the notebook skeleton
5. implement baseline CNN
6. run and log first experiment

## Working Principle
The project will prioritize clarity, reproducibility, and fair experimentation over unnecessary complexity. A smaller number of carefully designed experiments with strong analysis is preferred over many poorly controlled runs.