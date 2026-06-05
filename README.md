🐾 Dog vs Cat Image Classification using SVM

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat\&logo=python\&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.35+-FF4B4B?style=flat\&logo=streamlit\&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-1.3+-F7931E?style=flat\&logo=scikitlearn\&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)

A **Machine Learning web application** that classifies images as either a **Dog 🐶** or **Cat 🐱** using a **Support Vector Machine (SVM)**. Built with **Python, Streamlit, and Scikit-learn**, this project demonstrates image preprocessing, machine learning model training, evaluation, and deployment through an interactive dashboard.

---

## ✨ Features

| Feature                  | Description                                         |
| ------------------------ | --------------------------------------------------- |
| 🧠 SVM Classifier        | RBF-kernel SVM with probability calibration         |
| ⚙️ Image Preprocessing   | Grayscale conversion, 64×64 resizing, normalization |
| 🔍 Live Prediction       | Upload an image and get instant classification      |
| 📊 Interactive Dashboard | User-friendly Streamlit interface                   |
| 📈 Evaluation Metrics    | Accuracy, Precision, Recall, F1-Score               |
| 📉 Visualizations        | Confusion Matrix and performance charts             |
| 💾 Model Persistence     | Save and load trained models using Pickle           |
| ⬇️ Export Support        | Download model and metrics report                   |

---

## 📂 Project Structure

```bash
Dog_Cat_Classification/
│
├── app.py
├── train_model.py
├── model.pkl
├── metrics.json
├── requirements.txt
├── README.md
│
├── dataset/
│   ├── cats/
│   └── dogs/
│
├── images/
└── assets/
```

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/dog-cat-classification.git
cd dog-cat-classification
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Add Dataset

Place cat and dog images inside:

```bash
dataset/
├── cats/
└── dogs/
```

Dataset Source:

https://www.kaggle.com/c/dogs-vs-cats/data

### 5️⃣ Train the Model

```bash
python train_model.py
```

Generated files:

```bash
model.pkl
metrics.json
```

### 6️⃣ Run the Application

```bash
streamlit run app.py
```

Open:

```bash
http://localhost:8501
```

---

## 🔬 Machine Learning Pipeline

```text
Raw Image
    ↓
Grayscale Conversion
    ↓
Resize (64×64)
    ↓
Flatten
    ↓
StandardScaler
    ↓
SVM Classifier
    ↓
Prediction
```

---

## 🧠 Support Vector Machine (SVM)

The model uses an **RBF (Radial Basis Function) Kernel** to classify images.

### Hyperparameters

```python
SVC(
    kernel="rbf",
    C=10,
    gamma="scale",
    probability=True
)
```

### Why SVM?

* Effective for binary classification
* Works well with high-dimensional data
* Generates robust decision boundaries
* Provides confidence scores through probability calibration

---

## 🖼️ Image Preprocessing

### Steps Performed

1. Read image using OpenCV
2. Convert RGB image to Grayscale
3. Resize image to 64×64
4. Flatten into 4096-dimensional vector
5. Normalize using StandardScaler
6. Feed into trained SVM model

---

## 📊 Technologies Used

| Technology   | Purpose                   |
| ------------ | ------------------------- |
| Python       | Core Programming Language |
| Streamlit    | Web Application           |
| Scikit-Learn | Machine Learning          |
| OpenCV       | Image Processing          |
| NumPy        | Numerical Computation     |
| Pandas       | Data Handling             |
| Matplotlib   | Visualization             |
| Seaborn      | Heatmaps & Charts         |
| Pillow       | Image Loading             |

---

## 📈 Expected Performance

| Dataset Size      | Accuracy |
| ----------------- | -------- |
| 200 Images/Class  | ~68%     |
| 500 Images/Class  | ~74%     |
| 1000 Images/Class | ~80%     |

> Performance improves as training data increases.

---

## 🚀 Future Improvements

* CNN-Based Classification
* Transfer Learning (ResNet50, VGG16)
* HOG Feature Extraction
* Hyperparameter Tuning
* Real-Time Webcam Prediction
* Docker Deployment
* FastAPI Integration
* MLflow Model Tracking

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🙌 Acknowledgements

* Kaggle Dogs vs Cats Dataset
* Scikit-Learn Documentation
* Streamlit Community
* OpenCV Documentation

---

### ⭐ If you found this project useful, don't forget to Star the Repository!

**Made with ❤️ by Mayank **
