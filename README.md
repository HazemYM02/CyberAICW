# FaceGuard: AI-Based Access Control with Adversarial Testing

This project presents a complete pipeline for building, evaluating, attacking, and defending an AI-based facial recognition system called FaceGuard, inspired by real-world access control use cases in cybersecurity.

It includes:
	•	A CNN for face recognition using the Extended Olivetti Faces dataset.
	•	A function for access control (Access_Control) granting or denying entry to specific individuals.
	•	Adversarial robustness evaluation using FGSM attacks (targeted & untargeted).
	•	Defense via adversarial training.

⸻

Features
	•	🧠 Face Recognition CNN
Custom CNN trained to classify 40 individuals using grayscale face images (64×64).
	•	🔐 Access Control System
Implements logic to only grant access to authorized personnel (IDs 0, 5, and 10).
	•	🧪 Adversarial Testing
	•	Untargeted FGSM Attack: Evaluates model robustness against increasing ε (epsilon) values.
	•	Targeted FGSM Attack: Forces misclassification to gain unauthorized access.
	•	🛡 Adversarial Training (Blue Team)
Retrains model using adversarial examples to improve resistance to attacks.

⸻

🛠 Installation

🔧 Requirements

pip install torch torchvision numpy matplotlib scikit-learn pillow


⸻

🚀 How to Run
	1.	Launch the notebook:

jupyter notebook CW.ipynb


	2.	Run through the sections:
	•	CNN Definition & Training
	•	Model Evaluation
	•	Access Control Logic
	•	FGSM Attacks (Targeted & Untargeted)
	•	Adversarial Training and Comparison

⸻

📊 Sample Results
	•	Accuracy Plot: Model performance over training epochs.
	•	Access Logs: Console output of “Access Granted” or “Access Denied”.
	•	Adversarial Visuals: Comparison between original and perturbed inputs.
	•	Epsilon vs Accuracy: Visualization of model robustness under FGSM.

⸻

🔍 Use Case

This project simulates a real-world cybersecurity scenario: securing access to a sensitive area using AI and understanding its vulnerabilities through red team (attack) and blue team (defense) strategies.

⸻
