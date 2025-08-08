# 🛰️ Land Cover Classification using Satellite Imagery (EuroSAT)

This project focuses on developing a robust, scalable deep learning pipeline to classify land cover types such as forests, croplands, urban areas, and water bodies from satellite images. We used the EuroSAT dataset and implemented both baseline CNNs and transfer learning models to achieve state-of-the-art performance.

## 🎯 Project Goal

To build an accurate and reliable machine learning system capable of classifying land cover types using satellite images—targeting real-world applications in agriculture, urban planning, and environmental monitoring.

---

## 📦 Dataset

- **Name**: [EuroSAT Dataset](https://www.kaggle.com/datasets/apollo2506/eurosat-dataset)
- **Classes**: 10 (e.g., AnnualCrop, Forest, River, Residential, etc.)
- **Image Size**: Resized to 64×64 RGB
- **Split**: 70% Training | 20% Validation | 10% Testing

---

## 🧪 Model Development

### 1. Baseline CNN
- Achieved ~82% accuracy with a simple custom CNN.
- Helped establish foundational expectations and training metrics.

### 2. Transfer Learning
- Implemented VGG16, VGG19, and ResNet50 using ImageNet pre-trained weights.
- VGG19 and ResNet50 achieved **98.25%+ and ~98.4%** accuracy respectively.

### 3. Robustness Testing
- Applied **AugMix** and **FGSM adversarial attacks**.
- Observed 15–17% accuracy drop in unregularized models.
- Used **L2 regularization** to enhance adversarial robustness:
  - Regularized VGG16 retained **~87% accuracy** under FGSM.

---

## 📈 Results Summary

| Model           | Accuracy | Notes                         |
|----------------|----------|-------------------------------|
| Shallow CNN     | ~82%     | Baseline                      |
| VGG16 (pretrained) | ~98%     | Excellent generalization      |
| VGG19           | 98.25%   | Best performer overall        |
| ResNet50        | ~98.4%   | Matches literature benchmarks |
| VGG16 + FGSM    | ~81%     | Accuracy under attack         |
| VGG16 (L2) + FGSM | ~87%     | Improved robustness           |

---

## ⚙️ Tech Stack

- Python, Keras, TensorFlow
- NumPy, Pandas, Matplotlib
- Jupyter Notebook / Google Colab

---

## 🚀 Use Cases

- Agricultural land type analysis
- Urban growth monitoring
- Environmental and climate change modeling

---

## 📄 Project Report

- [View Project Presentation (PDF)](https://docs.google.com/presentation/d/1B9wKi_e0ep9A0XUaOAoqPJgI0GHxUhpU/edit?usp=sharing&ouid=114973997576517566639&rtpof=true&sd=true)

---

## 🙌 Authors

- **Lokesh Joshi**, PDPM IIITDM Jabalpur  
Feel free to reach out via [LinkedIn](https://www.linkedin.com/in/lokesh-j-819181336/)
