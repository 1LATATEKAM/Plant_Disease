🌱 Plant Disease Detection System

  A machine learning-based system to detect whether a plant leaf is healthy or diseased using image classification.

🚀 Features
        📷 Image-based plant health detection
        🤖 Machine Learning model using MobileNetV2
        ⚡ Fast prediction using API
        🌿 Works for Lemon and Spider plants
        🔌 Can be integrated with IoT devices (ESP32 Camera)

🧠 Machine Learning Model
          Model: MobileNetV2 (Transfer Learning)
          Classes: Healthy and Diseased
          Dataset: Custom dataset (Lemon + Spider plant images)
          Accuracy: ~70% (trained on small dataset)
          Techniques used:
          Data Augmentation
          Image preprocessing
          Transfer Learning

📁 Project Structure
          plant-disease-api/
          │── ml_model/
          │── train.py
          │── predict.py
          │── app.py
          │── README.md

⚙️ How It Works
          Image is captured (ESP32 / user upload)
          Image is sent to API
          ML model processes the image
          Output: Healthy or Diseased



          Algorithm Steps for ML part
-Start
-Input Image
  Capture or upload an image of the plant leaf
-Preprocess Image
  Resize image to 224 × 224 pixels
  Normalize pixel values (scale between 0 and 1)
-Load Pre-trained Model
  Load MobileNetV2 model without top layers
  Freeze base layers (to retain learned features)
-Feature Extraction
  Pass the image through MobileNetV2
  Extract features like texture, color, and patterns
-Add Classification Layers
  Add:
    Global Average Pooling layer
    Dense layer (ReLU activation)
    Output layer (Softmax activation)
-Train Model
  Train using labeled dataset:
    Class 1 → Healthy
    Class 2 → Diseased
  Use data augmentation to improve performance
-Model Prediction
  Input new image
  Model predicts class probabilities
-Output Result
  Display:
    Predicted class (Healthy / Diseased)
    Confidence percentage
-End


“Due to limited dataset availability, the model was optimized using augmentation and transfer learning techniques.”
