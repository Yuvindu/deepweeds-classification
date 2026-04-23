# Dataset Notes

## Dataset Name
DeepWeeds

## Task Type
Multi-class image classification

## Domain
Agricultural computer vision / weed species recognition

## Dataset Summary
DeepWeeds is a public image dataset for classifying weed species from field images captured in natural outdoor conditions. It is more realistic than toy or studio-style datasets because the images include background clutter, lighting variation, and natural scene complexity.

## Why This Dataset Was Chosen
- more unique than common image classification datasets such as pets or flowers
- realistic real-world application in agriculture
- suitable for CNNs and transfer learning
- manageable for Google Colab
- supports a clear baseline vs improvement comparison

## Classification Goal
The goal is to predict the weed species shown in each image.

## Expected Challenges
- natural background clutter
- variation in lighting and viewpoint
- possible visual similarity between some weed classes
- field conditions that make classification harder than standard object datasets

## Planned Use in This Project
This dataset will be used to compare:
1. a custom CNN trained from scratch
2. a pretrained ResNet-18 with frozen backbone
3. a fine-tuned pretrained ResNet-18

## Split Strategy
The dataset will be divided into:
- training set
- validation set
- test set

Planned starting split:
- 70% training
- 15% validation
- 15% test

If an official split is available and practical, that will be considered first. Otherwise, a stratified split will be created to preserve class balance as much as possible.

## Planned Preprocessing
- resize all images to 224 x 224
- convert images to tensors
- normalize pixel values
- ensure consistent label encoding

## Planned Data Augmentation
Training data only:
- random horizontal flip
- small random rotation
- random resized crop
- optional light color jitter if needed

Validation and test data will not use augmentation other than resizing and normalization.

## Planned Evaluation Metrics
- accuracy
- macro precision
- macro recall
- macro F1-score
- confusion matrix

## Notes to Fill In After Dataset Inspection
- exact number of classes
- class names
- total number of images
- class distribution
- source / citation details
- whether there are duplicate or low-quality samples
- whether an official split exists
- sample image observations