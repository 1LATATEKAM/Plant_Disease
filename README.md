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

“Due to limited dataset availability, the model was optimized using augmentation and transfer learning techniques.”
