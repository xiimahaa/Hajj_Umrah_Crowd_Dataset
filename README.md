# Hajj & Umrah Crowd Density Detection

An Intelligent System project that utilizes Computer Vision and Machine Learning to monitor and classify crowd density in the Holy Sites (High, Medium, and Low). 
This project compares traditional Image Processing techniques with modern Deep Learning architectures.

---

## 📌 Project Overview

Crowd management is a critical safety factor during Hajj and Umrah. 
This system provides an automated way to analyze live or recorded footage to assist authorities in managing pedestrian flow and preventing overcrowding.

---
## 📊 Dataset
The system was trained and validated using a custom dataset categorized into three levels of crowd density.

* **High Crowd:** Dense concentrations of pilgrims (e.g., Mataf during peak hours).
* **Medium Crowd:** Moderate flow with visible ground space.
* **Low Crowd:** Sparse density with high mobility.

**Class Distribution:**
* High Crowd: 15 images
* Medium Crowd: 16 images
* Low Crowd: 17 images
* **Total:** 48 images (augmented during CNN training to increase volume).

---

## 🛠️ Technologies Used

- 1. Image Processing & Preprocessing
Resize & Grayscale: Standardizing inputs for model consistency.
Gaussian Blur: Removing noise and smoothing images.
Histogram Equalization: Enhancing contrast to highlight crowd textures.
Otsu’s Thresholding: Automated foreground/background separation.
Morphological Operations: Noise reduction and region continuity.

- 2. Classical Machine Learning
Features: Manual extraction of Crowd Area, Crowd Percentage, and Edge Pixels.
Models: Implementation and evaluation of KNN, SVM, and Random Forest.
Best Baseline Performance: Random Forest achieved 66% accuracy.

- 3. Deep Learning (CNN)
Architecture: Utilized MobileNetV2 with Transfer Learning.
Data Augmentation: Implemented image flipping and rotation to handle the small dataset size (approx. 48 images).
Classification: Optimized for 3-class classification (High, Medium, Low).

---
## Tech Stack
- Language: Python
- Libraries: OpenCV, Scikit-Learn, TensorFlow/Keras, NumPy, Pandas, Matplotlib
- Environment: Jupyter Notebook / Anaconda


## 📈 Model Comparison Results
| Model | Accuracy |
|------|----------|
| Random Forest | 66.0% |
| CNN | 88.5% |


## 📁 Project Structure
Hajj_Umrah_Crowd_Detection/
│  
├── imageproject.ipynb              # Main Jupyter Notebook 
├── hajj_crowd_cnn_model.h5         # Trained CNN Model file
│  
├── Hajj_Umrah_Crowd_Dataset/       # Dataset folder
│   └──  high_crowd/                 # Images with high density 
│   └──  medium_crowd/               # Images with MEDIUM density 
│   └──  low_crowd/               # Images with low density 
└── README.md                       # Project documentation

