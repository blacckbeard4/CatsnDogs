# 🐶🐱 Cats vs Dogs - Image Classification

Welcome to my submission for the [Kaggle Dogs vs. Cats Redux](https://www.kaggle.com/competitions/dogs-vs-cats-redux-kernels-edition) classification challenge!

This project demonstrates how to build progressively better deep learning models to distinguish between images of cats and dogs. The final submission predicts the **probability** that an image contains a dog — evaluated via **log loss** on Kaggle.

---

## 🎯 Objective

Develop a binary classifier that assigns a probability score to each test image, indicating whether it's a dog (`1.0`) or a cat (`0.0`).

---
## 🔍 Sample Visuals

### 📷 Sample Training Images

<img width="332" height="242" alt="image" src="https://github.com/user-attachments/assets/96dcbf3b-d18b-4894-950b-b3293d11c23d" /> 
<img width="332" height="242" alt="image" src="https://github.com/user-attachments/assets/18017e0d-2e21-48b7-8d29-37ee0557a7ef" />
<img width="332" height="242" alt="image" src="https://github.com/user-attachments/assets/eb3f31fa-b13f-4eba-bbb0-55eaff28d4e4" /> 
<img width="332" height="242" alt="image" src="https://github.com/user-attachments/assets/75cfe60a-9e14-4fd5-a09d-1b8b11422d75" />
<img width="332" height="242" alt="image" src="https://github.com/user-attachments/assets/38ecf6ab-c06a-47b5-9115-60e6aa60b20b" />
<img width="332" height="242" alt="image" src="https://github.com/user-attachments/assets/7ee65c37-21f9-45da-ba31-9d172652276a" />





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
