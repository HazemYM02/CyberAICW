# FaceGuard: AI-Based Access Control with Adversarial Testing

This repository contains a complete implementation of a facial recognition-based access control system called **FaceGuard**, built using PyTorch. It demonstrates how adversarial attacks can compromise such systems and how to defend against them using adversarial training.

---

##  Overview

FaceGuard is designed to control access to a sensitive server room by identifying personnel using facial recognition. Only authorized users (IDs `0`, `5`, and `10`) are allowed access. This project includes:

- A CNN model for facial classification
- An access control system based on model predictions
- Targeted and untargeted FGSM adversarial attacks
- Adversarial training to improve robustness



## Features

- 🧠 **Face Recognition CNN**  
  Custom CNN trained to classify 40 individuals using grayscale face images (64×64).

- 🔐 **Access Control System**  
  Implements logic to only grant access to authorized personnel (IDs `0`, `5`, and `10`).

- 🧪 **Adversarial Testing**
  - **Untargeted FGSM Attack**: Evaluates model robustness against increasing ε (epsilon) values.
  - **Targeted FGSM Attack**: Forces the model to misclassify input as a specific authorized user.

- 🛡 **Adversarial Training (Blue Team)**  
  Retrains the model using adversarial examples to improve resistance to attacks and enhance system robustness.



## 🛠 Installation

### Requirements

Install required Python packages:

```bash
pip install torch torchvision numpy matplotlib scikit-learn pillow
```
##  Usage

### Follow these steps to run the project:
#### Clone the repository
```bash
git clone https://github.com/yourusername/faceguard-fgsm-attacks.git
cd faceguard-fgsm-attacks
```
### Start Jupyter Notebook
```bash
jupyter notebook CW.ipynb
```
### Execute the notebook sections
✅ **Model Training** 
- Trains a CNN using the augmented Olivetti face dataset.
- Plots training loss over epochs.
  
📈 **Model Evaluation**
- Tests accuracy on the unseen dataset.
- Prints classification results.
  
🔐 **Access Control**
- Runs predictions for selected individuals.
- Prints “Access Granted” or “Access Denied” based on their ID.
  
⚠️ **Untargeted FGSM Attack**
- Applies adversarial perturbations with increasing epsilon.
- Plots how accuracy drops as noise increases.
  
🎯 **Targeted FGSM Attack**
- Generates adversarial images to impersonate an authorized user.
- Attempts to bypass access control.
  
🛡 **Adversarial Training**
- Retrains the model with adversarial examples.
- Compares robustness with the original model using accuracy vs epsilon plots.

### Results
- 📉 Training Loss: Tracked and visualized over 50 epochs.
- 🧪 FGSM Attacks: Visualizations of adversarial examples.
- 📈 Accuracy vs Epsilon: Evaluates how noise impacts classification.
- ✅ Access Decisions: System prints “Access Granted” or “Access Denied” for test images.

