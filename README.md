✋ Hand Gesture Recognition Model

📌 Project Overview

This project implements a real-time hand gesture recognition system powered by a Convolutional Neural Network (CNN) trained on the LeapGestRecog Dataset
.

The trained model is integrated with OpenCV and PyCAW to control the system volume using hand gestures detected live via webcam.

🔄 Workflow

Image loading & preprocessing

CNN model training on gesture images

Model evaluation (accuracy, confusion matrix, classification report)

Real-time gesture detection with webcam

Mapping gestures → system volume control (mute, unmute, increase, decrease)

📊 Dataset

Source:
LeapGestRecog Dataset

Folder Structure:

LeapGestRecog/
  00/
  01/
  ...
  09/


Classes (subset used for control):

✊ Fist → Mute 🔇

🖐 Palm → Unmute 🔊

👍 Thumbs Up → Volume Up ⬆️

👎 Thumbs Down → Volume Down ⬇️

Image Preprocessing:

Grayscale conversion

Resized to 64 × 64

Normalized pixel values [0,1]

🧮 Model Features

Architecture: CNN (3 Conv layers + BatchNorm + Dense layers)

Input size: 64 × 64 grayscale

Output labels: 10 gesture classes (4 used for volume mapping)

Training:

Optimizer: Adam

Loss: Categorical Crossentropy

Epochs: 20

Batch size: 32

⚙️ Requirements

Python 3.x

Libraries:

tensorflow

opencv-python

numpy

matplotlib

scikit-learn

mediapipe

pycaw

📥 Install all dependencies:

pip install -r requirements.txt

🔬 Methodology

1️⃣ Data Loading

Load images from LeapGestRecog dataset

Assign labels based on folder structure

2️⃣ Preprocessing

Convert to grayscale

Resize to 64×64

Normalize pixel values

3️⃣ Model Training

Train CNN on gesture images

Save trained model as handGesture_model.keras

4️⃣ Evaluation

Accuracy & loss curves

Confusion matrix

Classification report

5️⃣ Real-Time Gesture Control

Capture webcam feed with OpenCV

Detect hand region using MediaPipe

Predict gesture inside ROI

Map gestures to volume actions

📈 Results

Accuracy: ~98–99% on test set (10 classes)

Performance: Stable real-time gesture recognition (~15–20 FPS)

Volume Control: Smooth adjustment with natural gestures

✅ Example:

Palm → Unmute

Fist → Mute

Thumbs Up → Increase volume

Thumbs Down → Decrease volume

🔮 Future Improvements

Extend support to more gestures (Peace ✌, OK 👌, etc.)

Improve robustness with better ROI extraction

Use transfer learning (MobileNetV2, EfficientNet) for higher accuracy

Deploy as a desktop app with PyQt or web app with Streamlit/Flask

