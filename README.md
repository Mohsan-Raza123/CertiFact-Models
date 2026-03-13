# CertiFact: Deepfake Detection Models 🧠🔍

> **Part of the 🥈 2nd Place Award-Winning FYP: CertiFact Full-Stack System**

## 📌 Repository Overview
This repository contains the pre-trained deep learning models used in the **CertiFact** deepfake detection system. Due to their size, these models are hosted separately from the main application code using Git Large File Storage (LFS).

These models are trained to analyze facial artifacts, temporal inconsistencies, and spatial anomalies to classify media as authentic or AI-generated.

## 📂 Models Included
* `best_finetuned_xception.h5` - Fine-tuned Xception network for frame-by-frame spatial manipulation detection.
* `final_xception_model.keras` - The final compiled Keras format of the Xception model.
* `deepfake_lstm_final.h5` - LSTM sequence model used for detecting temporal inconsistencies across video frames.
* `deepfake_face_detector.h5` - Specialized model for cropping and isolating facial regions before classification.
* `deepfake_detector_v6_final_stable.h5` - The stable, production-ready ensemble model used in the main backend.

## ⚙️ How to Download (Important!)
Because these files are large, standard `git clone` will only download tiny text pointers. You **must** have [Git LFS](https://git-lfs.github.com/) installed to download the actual model weights.

\`\`\`bash
# 1. Install Git LFS (if you haven't already)
git lfs install

# 2. Clone the repository
git clone https://github.com/Mohsan-Raza123/CertiFact-Models.git

# 3. Pull the large files
cd CertiFact-Models
git lfs pull
\`\`\`

## 🚀 How to Load in Python
Ensure you have TensorFlow/Keras installed (`pip install tensorflow`).

\`\`\`python
import tensorflow as tf

# Load an .h5 model
stable_model = tf.keras.models.load_model('deepfake_detector_v6_final_stable.h5')

# Load a .keras model
keras_model = tf.keras.models.load_model('final_xception_model.keras')

# Example prediction (assuming 'processed_face' is a preprocessed image array)
# prediction = stable_model.predict(processed_face)
\`\`\`

## 🔗 Main Project
To see these models in action within a full-stack React and Python web application, visit the main repository:
[CertiFact-Deepfake-Detection](https://github.com/Mohsan-Raza123/CertiFact-Deepfake-Detection)

## 👨‍💻 Author
**Mohsan Raza**
* BS Computer Science Graduate 
* [Link to your LinkedIn Profile]
