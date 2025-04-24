# 🧠 Comparative Analysis: Custom CNN vs Transfer Learning with Fine-Tuning

This project evaluates and compares the performance of two deep learning approaches for classifying English Premier League team logos:

1. **Custom Convolutional Neural Network (CNN)** – Built from scratch using Keras
2. **Transfer Learning with Fine-Tuning** – Using a pretrained MobileNetV2 model

The main goal is to identify which approach better generalizes to real-world test images, considering the specific visual characteristics of football team logos (e.g., vector-like design, white backgrounds, symmetry).

---

## 🗂️ Project Structure

dataset/ #trainigset with 20k images from Premier league teams -> Link: https://www.kaggle.com/datasets/alexteboul/english-premier-league-logo-detection-20k-images/code
Imagens_teste/ #Images collected from the internet to test the model on interative basis
cnn_robusta_com_augmentation.ipynb #CNN trained from scratch
mobilenetv2_transfer_learning_completo.ipynb #CNN trained using TL and Fine-Tuning Techniques
