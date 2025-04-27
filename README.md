# 🍔 Food Image Classification using VGG16

[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)](https://www.tensorflow.org/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.7%2B-blue?logo=python)](https://www.python.org/)

A deep learning project to classify food images into 5 categories using **VGG16 transfer learning** and **TensorFlow 2.x**.

---

## 📂 Project Structure

- **Step 1:** Clean and filter valid images.
- **Step 2:** Load train and validation datasets with a 70/30 split.
- **Step 3:** Prefetch datasets for efficient training.
- **Step 4:** Build a CNN model with VGG16 as the backbone.
- **Step 5:** Train the model and evaluate performance.

---

## ⚙️ Requirements

- Python 3.7 or newer
- TensorFlow 2.x
- Pillow (PIL)

Install the requirements:

```bash
pip install tensorflow pillow
```

---

## 📊 Dataset

- **Source:** [Kaggle - Food Image Classification Dataset](https://www.kaggle.com/datasets)
- **Selected Classes:** 
  - Baked Potato
  - Crispy Chicken
  - Donut
  - Fries
  - Hot Dog

- **Structure:**

```
/Food Classification dataset
    /Baked Potato
    /Crispy Chicken
    /Donut
    /Fries
    /Hot Dog
```

✅ Only valid JPEG, PNG, BMP images are loaded.  
❌ Corrupted images are automatically skipped.

---

## 🧠 Model Architecture

| Layer | Details |
|:-----:|:--------|
| Input | 256x256 RGB Images |
| Rescaling | Pixel values normalized [0,1] |
| VGG16 | Pre-trained on ImageNet, frozen |
| GlobalAveragePooling2D | Feature reduction |
| Dense (512) + Dropout (0.3) | Fully connected |
| Dense (256) + Dropout (0.3) | Fully connected |
| Dense (128) + Dropout (0.2) | Fully connected |
| Dense (64) + Dropout (0.2) | Fully connected |
| Output (5 classes) | Softmax activation |

---

## 🚀 How to Run

1. Update the dataset path in the script:

```python
original_data_dir = "/kaggle/input/food-image-classification-dataset/Food Classification dataset"
```

2. Run the full notebook/script.

3. Training will begin automatically and report accuracy/validation metrics.

---

## 📈 Future Enhancements

- Data Augmentation (flip, rotate, zoom)
- Fine-tune VGG16 (unfreeze last few layers)
- Learning Rate Scheduling
- Early Stopping and Model Checkpointing
- Export trained model (`.h5`, `.tflite`, etc.)

---

## 📜 License

This project is licensed under the **MIT License**.  
Dataset usage should comply with the [original Kaggle dataset license](https://www.kaggle.com/datasets).

---

# 📷 Sample Results

*(Optional section: Add model accuracy graphs or some prediction samples once you have them!)*

---

Would you also like me to create a small **LICENSE** file (MIT license) for you too? 🚀  
It'll complete the GitHub repo nicely! 🌟
