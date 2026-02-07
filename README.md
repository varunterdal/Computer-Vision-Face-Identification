# 🐱 Cat Face Identification Using Classical Computer Vision Techniques

This project presents a **classical computer vision approach** for identifying cat faces in images using **handcrafted features** and **traditional machine learning algorithms**, without relying on deep learning models. The system demonstrates that interpretable and computationally efficient methods can still achieve high accuracy in real-world vision tasks.

📌 This work has also been extended into a **research paper selected at IEEE ITHREECTCON 2026**.

---

## 📄 Project Overview

- **Domain:** Computer Vision  
- **Approach:** Classical (Non-Deep Learning)  
- **Task:** Binary Classification (Cat Face vs Background)  
- **Techniques Used:**
  - Facial Landmark–Based Localization
  - Histogram of Oriented Gradients (HOG)
  - Support Vector Machine (SVM)

The project focuses on building an **explainable and efficient vision pipeline**, suitable for academic learning and environments with limited computational resources.

---

## 🎯 Objectives

- Detect and identify cat face regions in images
- Avoid deep learning models for better interpretability
- Use handcrafted features to understand visual structure
- Demonstrate strong performance using classical techniques

---

## 🗂 Dataset

- **Dataset:** Crawford Cat Dataset  
- **Annotations:** Facial landmark coordinates (eyes, nose, mouth)

Bounding boxes are **derived from landmarks**, ensuring accurate and consistent face localization without using learned detectors.

---

## 🧠 Methodology

### 1️⃣ Face Localization
- Facial landmark coordinates are parsed from annotation files
- Bounding boxes are computed using min–max landmark values
- Padding is applied to cover complete facial regions

### 2️⃣ Background Sample Generation
- Non-face patches are sampled from image regions
- Intersection over Union (IoU) ensures minimal overlap with face regions
- Forms a balanced binary classification dataset

### 3️⃣ Image Preprocessing
- Grayscale conversion
- Image resizing to **64 × 64**
- Noise reduction using Gaussian / Bilateral filtering

### 4️⃣ Feature Extraction
- **Histogram of Oriented Gradients (HOG)** is used
- Captures edge orientation and structural facial patterns
- Produces fixed-length feature vectors

### 5️⃣ Classification
- **Linear Support Vector Machine (SVM)**
- Chosen for:
  - High performance on handcrafted features
  - Low computational cost
  - Strong generalization ability

---

## 🏗 System Architecture

```

Input Image
↓
Landmark-Based Face Localization
↓
Face & Background Patch Extraction
↓
Image Preprocessing
↓
HOG Feature Extraction
↓
Linear SVM Classification
↓
Cat Face / Background Output

```

---

## 📊 Results

- **Classification Accuracy:** ~96%
- High precision and recall
- Robust against:
  - Pose variations
  - Lighting changes
  - Background clutter

The model consistently captures facial structures such as eyes and contours, leading to reliable cat face identification.

---

## 📁 Project Structure

```

cat-face-identification/
│
├── notebooks/
│   └── cat_face_identification.ipynb
│
├── images/
│   ├── sample_input.jpg
│   └── output_results.png
│
├── report/
│   └── Project_Report.pdf
│
├── requirements.txt
└── README.md

````

---

## 🧪 Technologies Used

- Python  
- OpenCV  
- NumPy  
- Matplotlib  
- Scikit-learn  

---

## 📑 Research Paper

**Title:**  
**Cat Face Identification Using Classical Computer Vision Techniques**

This research highlights the continued relevance of classical computer vision methods as a strong foundation for modern vision systems.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/cat-face-identification.git
````

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook:

   ```bash
   jupyter notebook
   ```

4. Run all cells to view results.


## 🎓 Academic Note

This project is intended for **educational and research purposes**, demonstrating classical computer vision techniques for face identification tasks.

## 👤 Author

**Varun S Terdal**
Computer Vision & Machine Learning Enthusiast

