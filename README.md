# 🐱🐶 Cat vs Dog Image Classifier

A deep learning project that classifies images as **Cat** or **Dog** using a Convolutional Neural Network (CNN) built with TensorFlow/Keras, trained and run on **Google Colab**.

---

## 📌 Project Overview

This project uses a CNN model to perform binary image classification between cats and dogs. The model is trained on a dataset loaded from Google Drive, includes data augmentation, and can predict on custom uploaded images.

---

## 🧠 Model Architecture

The CNN model consists of the following layers:

| Layer | Details |
|-------|---------|
| Conv2D | 32 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Conv2D | 64 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Conv2D | 128 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Flatten | — |
| Dense | 128 units, ReLU |
| Dense (Output) | 1 unit, Sigmoid |

- **Optimizer:** Adam  
- **Loss Function:** Binary Crossentropy  
- **Metric:** Accuracy  
- **Epochs:** 10  
- **Image Size:** 150×150  

---

## 📁 Dataset

- Dataset is stored in **Google Drive** as `archive.zip`
- It is extracted to `/content/dataset/animals/` in Colab
- Contains two classes: `cats` and `dogs`
- 80% Training / 20% Validation split

---

## 🚀 How to Run

### Step 1: Open in Google Colab
Click the badge below or open `Cat_vs_Dog_Correct.ipynb` directly in Google Colab.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

### Step 2: Mount Google Drive
```python
from google.colab import drive
drive.mount('/content/drive')
```

### Step 3: Upload Dataset
Place `archive.zip` in your **Google Drive root folder (MyDrive)** before running.

### Step 4: Run All Cells
Go to **Runtime → Run All** in Colab.

### Step 5: Test Your Own Image
At the end of the notebook, you can upload any image and the model will predict whether it's a **Cat 🐱** or a **Dog 🐶**.

---

## 📊 Results

- Training and validation **accuracy/loss graphs** are plotted after training.
- A **Confusion Matrix** is displayed to evaluate model performance.
- Final **Validation Accuracy** is printed after evaluation.

---

## 🛠️ Libraries Used

- `TensorFlow / Keras`
- `NumPy`
- `Matplotlib`
- `scikit-learn`
- `zipfile`, `os`

---

## 📂 Project Structure

```
Cat_vs_Dog_Correct.ipynb   ← Main Colab Notebook
README.md                  ← Project Documentation
```

---

## 👤 Author

Made with ❤️ using Google Colab and TensorFlow.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
