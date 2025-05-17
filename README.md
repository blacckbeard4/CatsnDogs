# 🐶🐱 Cats vs Dogs - Image Classification

Welcome to my submission for the [Kaggle Dogs vs. Cats Redux](https://www.kaggle.com/competitions/dogs-vs-cats-redux-kernels-edition) classification challenge!

This project demonstrates how to build progressively better deep learning models to distinguish between images of cats and dogs. The final submission predicts the **probability** that an image contains a dog — evaluated via **log loss** on Kaggle.

---

## 🎯 Objective

Develop a binary classifier that assigns a probability score to each test image, indicating whether it's a dog (`1.0`) or a cat (`0.0`).

---
## 🔍 Sample Visuals

### 📷 Sample Training Images

<p align="center">
  <img src="https://i.imgur.com/gO27TR0.png" width="200">
  <img src="https://i.imgur.com/a7hGBaF.png" width="200">
  <img src="https://i.imgur.com/0c9AhVr.png" width="200">
  <img src="https://i.imgur.com/0pgECPx.png" width="200">
</p>

## 🧠 Approach

### 🏗️ Baseline CNN (Keras)
- Custom ConvNet trained from scratch
- Data augmentation: horizontal flip, zoom
- 5-epoch training with early stopping
- Achieved ~0.25 log loss on validation

### 📦 Transfer Learning (EfficientNet)
- Pretrained embeddings from EfficientNet
- Classical neural net on top of frozen features
- Faster convergence, better generalization

---

## 📦 Dataset

- **Source**: Provided by Kaggle
- **Training images**: 25,000 JPEGs in the format `cat.123.jpg` or `dog.456.jpg`
- **Test images**: Unlabeled set used for leaderboard submission

---

## 🛠️ Tools & Libraries

- Python, TensorFlow/Keras
- EfficientNet-PyTorch
- Matplotlib, Seaborn, OpenCV
- Jupyter Notebooks, Kaggle Kernels

---

## 📊 Results

| Model              | Log Loss | Accuracy (Val) |
|-------------------|----------|----------------|
| Baseline CNN      | ~0.25    | ~90%           |
| EfficientNet Model| ~0.18    | ~93%           |

---

## 🧠 Key Learnings

- Data augmentation helps mitigate overfitting on small image datasets.
- Transfer learning (with EfficientNet) improves performance and training time.
- Simple binary classification pipelines can still be highly effective with the right preprocessing.

---


## 📬 Contact

Made with ❤️ by [Justin Varghese](https://github.com/blacckbeard4)  
Feel free to fork, star, or reach out if you liked this repo!
