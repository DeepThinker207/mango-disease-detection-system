# 🥭 Full-Stack AI Mango Disease Detection System

An AI-powered full-stack web application that performs **real-time mango leaf disease detection directly in the browser** and provides **AI-generated treatment plans** through a secure backend API.

This system is designed to assist farmers with early disease diagnosis and actionable solutions using deep learning and generative AI.

---

## 🌟 Key Features

### ⚡ Fast, In-Browser AI Detection
- Runs a trained **MobileNetV2 Deep Learning model** directly inside the user's browser using **ONNX.js**
- No need for server-side GPU processing
- Works efficiently even in low-connectivity rural environments

### 🎯 High-Accuracy Disease Diagnosis
- Built using **Transfer Learning**
- Fine-tuned on the **PlantVillage Dataset (38 Classes)**
- Provides high-confidence predictions for mango leaf diseases

### 🤖 AI-Powered Treatment Plans
- After disease detection, the system securely calls the **Gemini 2.5 Flash API**
- Generates step-by-step treatment advice for the detected disease
- Backend ensures all API interactions remain secure

### 🔐 Secure & Scalable Architecture
- All sensitive API keys are stored securely in backend `.env` files
- Flask-based backend prevents exposure of Gemini API keys
- Monolithic architecture for easy deployment and scalability

### 📱 Fully Responsive UI
- Built with **Tailwind CSS**
- Mobile-first design for better accessibility for farmers

---

## 🧠 AI Model Details

| Component            | Technology Used        |
|----------------------|------------------------|
| Model Architecture   | MobileNetV2 (CNN)      |
| Training Framework   | PyTorch                |
| Learning Method      | Transfer Learning      |
| Model Format         | ONNX                   |
| Runtime Engine       | ONNX.js                |
| Input Image Size     | 224 x 224              |

### 🔁 Transfer Learning Approach

We used **Feature Extraction-Based Transfer Learning** by leveraging a pre-trained MobileNetV2 model trained on the ImageNet dataset.

- The convolutional base layers were frozen  
- The final classification layer was modified  
- The model was retrained to classify plant leaf diseases from the PlantVillage dataset  

---

## 🖥️ System Workflow
Upload Mango Leaf Image
↓
Image Preprocessing
↓
ONNX Model Inference (Browser)
↓
Disease Prediction
↓
Flask Backend API Call
↓
Gemini AI Treatment Plan
↓
Solution Displayed to User


---

## 🛠️ Tech Stack

### Frontend (Client-Side)
- React (via CDN)
- ONNX.js
- Tailwind CSS
- JavaScript
- HTML5
- Babel (In-Browser JSX Transpiler)

### Backend (Server-Side)
- Python
- Flask
- Gunicorn (Production Deployment)

### Artificial Intelligence
- PyTorch (Model Training)
- MobileNetV2 (CNN Architecture)
- ONNX (Model Conversion)
- Gemini 2.5 Flash (Treatment Recommendation LLM)

---

## 📂 Dataset

Model training was performed on the **PlantVillage Dataset**, which contains labeled images of healthy and diseased plant leaves across multiple classes.

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/mango-disease-detection.git
cd mango-disease-detection