# Experiment Log

This file records all experimental runs for the DeepWeeds image classification project.  
Each entry should capture enough detail to reproduce the run and compare it fairly with other settings.

---

## Experiment Template

### Experiment ID
Example: EXP-001

### Date
YYYY-MM-DD

### Experiment Name
Short descriptive name

### Objective
What this run is trying to test.

### Model
- model type:
- baseline / transfer learning / fine-tuning:
- backbone (if any):

### Data Setup
- dataset:
- image size:
- split used:
- augmentation:
- class balancing used?:

### Training Configuration
- batch size:
- epochs:
- optimizer:
- learning rate:
- scheduler:
- loss function:
- early stopping:
- weight decay:
- dropout:

### Trainable Parameters
- frozen layers:
- unfrozen layers:
- classifier head details:

### Results
- best validation accuracy:
- best validation macro F1:
- test accuracy:
- test macro F1:
- training time:
- best epoch:

### Observations
- what worked:
- what did not work:
- signs of overfitting / underfitting:
- confusing classes:
- anything unexpected:

### Artifacts
- notebook:
- saved model path:
- plots:
- confusion matrix:
- notes:

---

## Experiments

### EXP-001
**Date:**  
**Experiment Name:** Baseline CNN

**Objective:**  
Establish the first baseline performance using a custom CNN trained from scratch.

**Model:**  
- model type: Custom CNN  
- baseline / transfer learning / fine-tuning: Baseline  
- backbone (if any): None  

**Data Setup:**  
- dataset: DeepWeeds  
- image size:  
- split used:  
- augmentation:  
- class balancing used?:  

**Training Configuration:**  
- batch size:  
- epochs:  
- optimizer:  
- learning rate:  
- scheduler:  
- loss function:  
- early stopping:  
- weight decay:  
- dropout:  

**Trainable Parameters:**  
- frozen layers: None  
- unfrozen layers: All  
- classifier head details:  

**Results:**  
- best validation accuracy:  
- best validation macro F1:  
- test accuracy:  
- test macro F1:  
- training time:  
- best epoch:  

**Observations:**  
- what worked:  
- what did not work:  
- signs of overfitting / underfitting:  
- confusing classes:  
- anything unexpected:  

**Artifacts:**  
- notebook:  
- saved model path:  
- plots:  
- confusion matrix:  
- notes:  

---

### EXP-002
**Date:**  
**Experiment Name:** ResNet-18 Frozen Backbone

**Objective:**  
Measure the effect of transfer learning using a pretrained model as a fixed feature extractor.

**Model:**  
- model type: ResNet-18  
- baseline / transfer learning / fine-tuning: Transfer learning  
- backbone (if any): Pretrained ResNet-18  

**Data Setup:**  
- dataset: DeepWeeds  
- image size:  
- split used:  
- augmentation:  
- class balancing used?:  

**Training Configuration:**  
- batch size:  
- epochs:  
- optimizer:  
- learning rate:  
- scheduler:  
- loss function:  
- early stopping:  
- weight decay:  
- dropout:  

**Trainable Parameters:**  
- frozen layers: Backbone  
- unfrozen layers: Classification head  
- classifier head details:  

**Results:**  
- best validation accuracy:  
- best validation macro F1:  
- test accuracy:  
- test macro F1:  
- training time:  
- best epoch:  

**Observations:**  
- what worked:  
- what did not work:  
- signs of overfitting / underfitting:  
- confusing classes:  
- anything unexpected:  

**Artifacts:**  
- notebook:  
- saved model path:  
- plots:  
- confusion matrix:  
- notes:  

---

### EXP-003
**Date:**  
**Experiment Name:** ResNet-18 Fine-Tuned

**Objective:**  
Test whether partial fine-tuning improves performance beyond frozen transfer learning.

**Model:**  
- model type: ResNet-18  
- baseline / transfer learning / fine-tuning: Fine-tuning  
- backbone (if any): Pretrained ResNet-18  

**Data Setup:**  
- dataset: DeepWeeds  
- image size:  
- split used:  
- augmentation:  
- class balancing used?:  

**Training Configuration:**  
- batch size:  
- epochs:  
- optimizer:  
- learning rate:  
- scheduler:  
- loss function:  
- early stopping:  
- weight decay:  
- dropout:  

**Trainable Parameters:**  
- frozen layers: Lower backbone layers  
- unfrozen layers: Upper backbone layers + classification head  
- classifier head details:  

**Results:**  
- best validation accuracy:  
- best validation macro F1:  
- test accuracy:  
- test macro F1:  
- training time:  
- best epoch:  

**Observations:**  
- what worked:  
- what did not work:  
- signs of overfitting / underfitting:  
- confusing classes:  
- anything unexpected:  

**Artifacts:**  
- notebook:  
- saved model path:  
- plots:  
- confusion matrix:  
- notes: