# Knowledge Distillation for Image Classification

This project demonstrates the use of **Knowledge Distillation (KD)** to train a compact and efficient student model using the guidance of a larger, more accurate teacher model.  
The main goal is to preserve classification accuracy while significantly reducing model complexity.

---

## 📌 Overview

Knowledge Distillation is a technique where a **student model** learns from both:
- The **hard labels** (true class labels), and
- The **soft targets** (logits or probabilities) produced by a **teacher model**.

In this project, we go a step further and also include **feature-based distillation**, where the student model tries to match internal feature representations of the teacher.

---

## 🧠 Key Features

- ✅ **Teacher model**: EfficientNet-B3  
- ✅ **Student model**: ResNet18 (with and without distillation for comparison)  
- ✅ **Datasets used**:
  - 3-class subset of CIFAR-10 (airplane, automobile, bird)
  - 2-class Chest X-ray dataset (normal vs pneumonia)
- ✅ **Distillation loss**: Combines:
  - Cross-entropy (hard labels)
  - KL-Divergence (soft labels)
  - Feature alignment (L2 loss)

---

## 🔬 Objectives

- Evaluate how well a smaller student model can perform with and without knowledge distillation.
- Compare the student model’s accuracy and efficiency against:
  - The original teacher model
  - The same student trained without distillation
- Analyze the impact of:
  - Varying temperature and alpha values
  - Using different types of loss (logits only vs. logits + features)

---

## 📊 Results Summary

- The student model trained **with distillation** consistently outperforms the same model **trained without it**.
- In some cases, the student even **outperformed the teacher** on the test set.
- Training time and model size were significantly reduced.

---

## 🛠️ Technologies

- Python
- PyTorch / Keras (depending on implementation)
- Google Colab
- Matplotlib, NumPy, scikit-learn

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Shani-rb/Distillation_project.git
2. Open the notebook in Google Colab:

SHANI.ipynb

3. Modify configuration cells to switch between:

Different datasets

Distillation vs. baseline mode

Temperature / alpha parameters

4. Run all cells to train and evaluate the models.
---
✍️ Author
Shani Bruck
Bioinformatics BSc Student @ Machon Tal – JCT
2025 Final Project

