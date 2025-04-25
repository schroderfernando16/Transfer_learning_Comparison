
# 🧠 Comparative Analysis: Custom CNN vs Transfer Learning with Fine-Tuning

This project evaluates and compares the performance of two deep learning approaches for classifying English Premier League team logos:

1. **Custom Convolutional Neural Network (CNN)** – Built from scratch using Keras  
2. **Transfer Learning with Fine-Tuning** – Using a pretrained MobileNetV2 model

The main goal is to identify which approach better generalizes to real-world test images, considering the specific visual characteristics of football team logos (e.g., vector-like design, white backgrounds, symmetry).

---

## 🗂️ Project Structure

```
.
├── dataset/                  # Training images organized by team (20 classes)
├── Imagens_Teste/           # Real-world logo test images (.jpg)
├── cnn_robusta_com_augmentation.ipynb
├── mobilenetv2_transfer_learning_completo.ipynb
└── modelo_mobilenetv2_finetuned.h5     # Final fine-tuned model
```

---

## 🔍 Highlights

### 🧪 Evaluation Metrics
- Accuracy on validation set
- Confusion matrix
- Test on custom real-world images (from `Imagens_Teste/`)

### 📈 Model Improvements
- For Transfer Learning: 
  - Augmentations tailored to logos (brightness, zoom, small rotation)
  - Fine-tuning of the last 50 layers of MobileNetV2
  - Learning rate control (1e-4 initially, 1e-5 during fine-tuning)
- For Custom CNN:
  - Multi-layer convolutional architecture
  - Dropout and MaxPooling layers
  - Realistic data augmentation strategies

---

## 🧠 Key Findings

| Model                     | Accuracy on Custom Test Set (24 images) |
|--------------------------|-----------------------------------------|
| Custom CNN (with Augmentations) | 87.5%                                 |
| MobileNetV2 (Fine-Tuned)  | 92%                                  |

Although the fine-tuned MobileNetV2 improved over the frozen model, the custom CNN still showed better generalization in this domain-specific task.

---

## 🚀 To Run on AWS SageMaker

- Upload the notebook: `mobilenetv2_transfer_learning_completo.ipynb`
- Upload the `dataset/` and `Imagens_Teste/` folders
- Use a kernel with TensorFlow 2.x
- Train and evaluate directly in the notebook

---

## 📌 Author

Fernando Schroder Rodrigues  
