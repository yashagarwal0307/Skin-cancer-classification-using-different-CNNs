---

# 🧬 Skin Cancer Detection using Deep Learning

Welcome to the Skin Cancer Detection project. This journey explores the potential of deep learning models in classifying different types of skin lesions using the HAM10000 dataset. The project aims to investigate how well neural networks can perform in a medically critical domain—and what their limitations are.

---

## 📌 Project Motivation

* Skin cancer is one of the most common cancers worldwide.
* Early detection is key to effective treatment.
* Manual diagnosis is time-consuming and subjective.
* The question: **Can deep learning models help in reliable, image-based skin cancer classification?**

---

## 📂 Dataset: Available on kaggle

* Contains **10,000+ dermatoscopic images** of **7 types of skin lesions**.
* Each image is labeled with one of the following categories:

  * Melanocytic nevi
  * Melanoma
  * Benign keratosis-like lesions
  * Basal cell carcinoma
  * Actinic keratoses
  * Vascular lesions
  * Dermatofibroma

---

## 🔍 Challenge Faced: **Imbalanced Dataset**

* The dataset was **heavily imbalanced**, with most images belonging to a few dominant classes.
* To counter this, I used **extensive data augmentation** (rotation, zoom, flips, brightness shifts, etc.) to **balance the dataset across all classes**.

---

## 🧪 Experiments and Models

### ✅ Tried the following CNN architectures:

* EfficientNetB0
* ResNet-50
* DenseNet201
* MobileNetV2

> 📈 **Best Single-Model Accuracy:** \~92%

Each model had strengths, but none surpassed the 92% barrier. That's when I decided to try something heavier...

---

## 🤝 Ensemble Approach

* Combined predictions from **5 models**:
  `EfficientNetB0 + ResNet-50 + DenseNet201 + MobileNetV2 + VGG-16`
* Ensemble was built using **soft voting** (averaging probabilities).

> 🚀 **Achieved Accuracy:** **93%**


* ⚠️ **Major drawback:** **Very high computational cost** — unrealistic for deployment or real-time use.

---

## 📉 Evaluation Metrics

For each model:

* Plotted **accuracy/loss curves**
* Generated **confusion matrices**
* Observed **class-wise performance**

These visualizations gave insight into where models succeeded or failed—especially in minority classes.

--- 
## Libraries used- Temsoflow, scikit-learn,numpy

## 🧠 Key Learnings

* **Medical image classification is hard** — models are sensitive to data quality and diversity.
* Even state-of-the-art models **struggled with certain classes**.
* **Images alone are not enough** — real-world diagnosis needs patient history, metadata, and expert insight.
* Ensemble models boost performance but aren’t always practical.



## 🚧 Future Work

* Explore **metadata fusion** (age, sex, lesion location) with images.
* Try **lightweight ensembling** (e.g., MobileNetV2 + EfficientNet only).
* Consider **self-supervised learning** or **contrastive pretraining**.
* Try integrating **transformers (e.g., ViT)**.

