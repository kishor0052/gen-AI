
# 🌱 GreenClassify

## Deep Learning-Based Vegetable Image Classification System

GreenClassify is an end-to-end deep learning web application that classifies vegetable images into **15 predefined categories** using a **Convolutional Neural Network (CNN)**.

The trained model is deployed using **Flask**, allowing users to upload images and receive **real-time predictions with confidence scores** through a clean and interactive web interface.

The system achieves **92.9% test accuracy**.

---

## 📌 Project Overview

This project demonstrates:

* Image classification using CNN
* Model training and evaluation
* Overfitting prevention using EarlyStopping
* Deployment of trained model using Flask
* Frontend integration using HTML, CSS, and JavaScript

---

## 🧠 Problem Statement

Manual vegetable classification in agriculture and retail environments is time-consuming and error-prone.

This project automates vegetable classification using deep learning techniques to improve efficiency and accuracy.

---

## 🎯 Objectives

* Understand Convolutional Neural Networks (CNNs)
* Preprocess image datasets for training
* Build and train a multi-class classification model
* Deploy the trained model as a web application
* Provide real-time predictions with confidence scores

---

## 📂 Dataset Information

**Dataset:** Vegetable Image Dataset (Kaggle)

* 15 vegetable classes
* 15,000 training images
* 3,000 validation images
* 3,000 test images

### Classes

Bean
Bitter_Gourd
Bottle_Gourd
Brinjal
Broccoli
Cabbage
Capsicum
Carrot
Cauliflower
Cucumber
Papaya
Potato
Pumpkin
Radish
Tomato

---

## ⚙️ Data Preprocessing

* Images resized to **150 × 150**
* Pixel values normalized (`rescale = 1/255`)
* Dataset split into train, validation, and test sets
* Implemented using `ImageDataGenerator`

---

## 🏗 Model Architecture

**Sequential CNN Model**

* Conv2D (32 filters, 3×3, ReLU)
* MaxPooling2D
* Conv2D (64 filters, 3×3, ReLU)
* MaxPooling2D
* Flatten
* Dense (128, ReLU)
* Dropout (0.25)
* Dense (128, ReLU)
* Dense (15, Softmax)

---

## 🏋️ Model Training

* **Optimizer:** Adam
* **Loss:** Categorical Crossentropy
* **Metric:** Accuracy
* **Batch Size:** 32
* **Max Epochs:** 30
* **EarlyStopping:** patience = 5

Training automatically stopped at **Epoch 9** to prevent overfitting.

---

## 📊 Model Performance

| Metric              | Value     |
| ------------------- | --------- |
| Training Accuracy   | ~96%      |
| Validation Accuracy | ~93–94%   |
| Test Accuracy       | **92.9%** |

---

## 🚀 Deployment

The trained model is deployed using Flask.

### Features

* Upload vegetable image
* Real-time prediction
* Confidence score display
* Clean and responsive UI
* Structured project architecture

---

## 📦 Model File

Due to GitHub's file size limitation (100MB), the trained model file
`vegetable_classification.h5` is hosted externally.

🔗 **Download Model Here:**


https://drive.google.com/drive/folders/1NJvDR5A0eSJjcc1vNf1XZHnooVM4gWLI?usp=sharing


After downloading, place the model file in the project **root directory** before running the application.

---

## 🖥 Application Flow

User → Upload Image → Flask → CNN Model → Prediction → Display Result

---

## 📁 Project Structure

```
GreenClassify/
│
├── app.py
├── vegetable_classification.h5
│
├── templates/
│   ├── index.html
│   ├── prediction.html
│   └── logout.html
│
├── static/
│   ├── css/
│   │   └── main.css
│   ├── js/
│   │   └── main.js
│   └── uploads/
│
└── README.md
```

---

## ▶️ How to Run Locally

### 1️⃣ Clone Repository

```
git clone https://github.com/Digvijay1009/GreenClassify.git
cd GreenClassify
```

### 2️⃣ Create Virtual Environment

```
python -m venv GC
GC\Scripts\activate   (Windows)
```

### 3️⃣ Install Dependencies

```
pip install flask tensorflow pillow numpy
```

### 4️⃣ Run Application

```
python app.py
```

Open in browser:

```
http://127.0.0.1:5000/
```

---

## ⚠️ Limitations

* Performs best on dataset-distributed images
* Accuracy may reduce on random internet images due to domain shift
* Does not support multiple vegetables in a single image

---

## 🔮 Future Enhancements

* Implement Transfer Learning (MobileNet / ResNet)
* Add Data Augmentation
* Display Top-3 predictions
* Deploy on cloud platform (Render / AWS / Heroku)
* Improve generalization for real-world images

---

## 📚 Technologies Used

* Python
* TensorFlow / Keras
* Flask
* HTML
* CSS
* JavaScript
* Google Colab

---

## 👨‍💻 Author

**Kishor**
Deep Learning & Computer Vision Project

---

