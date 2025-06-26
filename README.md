# Targeted and Untargeted FGSM on CAPTCHA

This project showcases how adversarial machine learning techniques—specifically the Fast Gradient Sign Method (FGSM)—can be used to perform targeted and untargeted attacks on a CAPTCHA recognition model.

Overview

CAPTCHAs are designed to distinguish humans from bots. However, modern deep learning models used to solve CAPTCHA challenges are vulnerable to adversarial attacks. This notebook demonstrates how to craft adversarial examples to:
	•	🚫 Mislead the model into incorrect predictions (untargeted attack)
	•	🎯 Force the model to output a specific incorrect label (targeted attack)

Both attack types are explored in detail using a convolutional neural network (CNN) and PyTorch.

Project Structure
	•	CW.ipynb: Main Jupyter Notebook containing model training, evaluation, and FGSM-based attacks.
	•	CNN model: A 3-layer convolutional network trained on CAPTCHA-like data.
	•	FGSM implementation: Attack logic using gradient-based perturbations.
	•	Visualization: Accuracy degradation plots and adversarial example previews.

⚙️ Requirements

Ensure the following Python packages are installed:
	•	torch
	•	numpy
	•	matplotlib
	•	PIL
	•	sklearn
	•	opencv-python (if needed for CAPTCHA generation)

Install via:

pip install torch numpy matplotlib pillow scikit-learn opencv-python

🚀 Usage
	1.	Clone the repository:

git clone https://github.com/yourusername/targeted-untargeted-fgsm-captcha.git
cd targeted-untargeted-fgsm-captcha


	2.	Launch the notebook:

jupyter notebook CW.ipynb


	3.	Follow the cells to:
	•	Train the CNN on CAPTCHA data
	•	Perform untargeted FGSM attacks and plot accuracy vs. epsilon
	•	Perform targeted FGSM attacks and visualize success

📊 Results
	•	Untargeted FGSM: Shows how increasing epsilon degrades model accuracy.
	•	Targeted FGSM: Demonstrates successful manipulation of model outputs toward attacker-chosen labels.

🔐 Security Insight

This project emphasizes the vulnerability of AI-based security systems to minimal, human-imperceptible perturbations, reinforcing the need for robust training and defense mechanisms.
