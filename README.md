# 🩺 Psoriasis Severity and Type Detection  
**A Deep Learning and Clustering-Based Approach for Psoriasis Analysis**

---

## 📘 Overview
**Psoriasis Severity and Type Detection** is an AI-driven dermatology system that analyzes skin images to identify different **types of psoriasis** — *Plaque, Guttate, Inversus, Pustular,* and *Erythrodermic* — and assess their **severity levels** using deep learning and clustering techniques.

The solution integrates:
- **Convolutional Neural Network (CNN)** for psoriasis type classification  
- **K-Means Clustering** for severity estimation  
- **Rule-Based Reasoning** for personalized **diet and medication recommendations**

The system is deployed using **Gradio** on **Hugging Face Spaces**, allowing users to upload images and receive instant predictions with care suggestions.

---

## 🧠 Key Features
- 🧬 **CNN-Based Image Classification** – Identifies psoriasis type from skin lesion images using TensorFlow/Keras.  
- 🔍 **Clustering-Based Severity Detection** – Categorizes cases as *Mild, Moderate,* or *Severe* using K-Means clustering.  
- 🩹 **Confidence Validation** – Applies a softmax probability threshold to ensure reliable predictions.  
- 🧾 **Expert Knowledge Integration** – Generates care recommendations based on classification and severity.  
- 💻 **Interactive Interface** – Built with Gradio for seamless user experience.  
- ☁️ **Cloud Deployment** – Hosted on Hugging Face Spaces for 24/7 accessibility.

---

## 🗂️ Dataset and Data Preparation
- **Source:** Curated from **Kaggle dermatology datasets** and clinical image repositories.  
- **Dataset Size:** 2,500+ labeled images representing five major psoriasis types.  
- **Data Split:**  
  - Training – 70%  
  - Validation – 15%  
  - Testing – 15%

### **Preprocessing Steps**
1. **Resizing:** All images standardized to `224×224` pixels.  
2. **Normalization:** Pixel values scaled to `[0, 1]`.  
3. **Augmentation:** Includes rotation, flipping, and zooming for variability.  
4. **Tensor Conversion:** Images converted into model-compatible tensors.

### **Quality Filtering**
- Low-quality or blurry images were automatically removed using:
  - **Resolution threshold (<224×224 pixels)**
  - **Variance of Laplacian method** for blur detection  
This ensures only high-quality, clinically meaningful images are used for training.

---

## 🧩 Model Architecture
### **1. CNN Classification**
- Learns visual features such as edges, textures, and lesion patterns.
- Outputs **softmax probabilities** across the five psoriasis types.

### **2. K-Means Clustering (Severity Detection)**
- Uses CNN-extracted feature vectors to group images by similarity.  
- Automatically assigns **severity levels**:  
  - *Mild* – Small or light patches  
  - *Moderate* – Noticeable inflammation  
  - *Severe* – Extensive scaling or redness

### **3. Rule-Based Reasoning**
- Combines classification and severity outputs to provide:
  - **Treatment suggestions** (e.g., topical corticosteroids, biologics)
  - **Diet recommendations** (omega-3 rich foods, vitamin D intake)

---

## 📈 Model Performance
- **Accuracy:** 94% across all psoriasis types  
- **Balanced Precision and Recall:** Reduces both false positives and negatives  
- **Confidence Threshold:** 85% for prediction validation  

---

## 🧰 Technologies Used
- **Programming Language:** Python  
- **Frameworks:** TensorFlow / Keras  
- **Machine Learning:** Scikit-learn (K-Means)  
- **Frontend:** Gradio  
- **Deployment:** Hugging Face Spaces  
- **Libraries:** NumPy, Pandas, OpenCV  

---

## 🚀 How to Run Locally

# Clone the repository
git clone https://github.com/Venisriyallampalli/Psoriasis-Severity-and-Type-Detection.git
cd Psoriasis-Severity-and-Type-Detection

# Install dependencies
pip install -r requirements.txt

# Run the application
python app.py

