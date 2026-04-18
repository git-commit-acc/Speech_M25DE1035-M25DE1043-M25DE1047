# 🎙️ Retrieval-based Voice Conversion (RVC) Pipeline

A **robust, production-ready implementation** of the Retrieval-based Voice Conversion (RVC) system, optimized for modern environments including **Kaggle (Tesla P100)**, **Google Colab**, and **local development setups**.

---

## 👥 Authors (Team)

- **Ajinkya Ghodake (M25DE1035)**
- **Vinit Nagar (M25DE1043)**
- **Ashish Sinha (M25DE1047)**

---

## 🚀 Overview

This project implements a **Speech-to-Speech (STS) Voice Conversion Pipeline** using RVC, with major enhancements to ensure:

- ✅ Python 3.10–3.12 compatibility  
- ✅ Stable execution in Colab/Kaggle  
- ✅ Reduced dependency conflicts  
- ✅ Automated model + environment setup  

---

## ⚙️ Key Features & Enhancements

### 🔧 Environment Fixes
- Removed incompatible version pinning (`numpy`, `numba`, `faiss`)
- Fully compatible with **Python 3.12**
- Stable execution across cloud environments

### ⚡ GPU Optimization
- Optimized for **Tesla P100 (sm_60)**
- Works on T4, V100, and CPU fallback

### 🧠 Fairseq Mocking
- Eliminates dependency issues
- Maintains HuBERT feature extraction

### 🔐 Security Patch
- Fixes PyTorch `UnpicklingError` (`weights_only` issue)

### 📦 Automated Model Handling
- Auto-download for:
  - HuBERT
  - RMVPE
  - Pretrained RVC models

---

## 📂 Project Structure


---

## 🎙️ Usage (Inference)

1. Load pipeline  
2. Place `.pth` model in `assets/weights/`  
3. Provide input audio  
4. Configure parameters  
5. Run conversion  

---

### 📊 Observations

- ✔️ Voice timbre successfully transformed  
- ✔️ Pitch consistency maintained  
- ✔️ Minimal distortion using `rmvpe`  
- ✔️ Best results with `index_rate ≈ 0.75`

---

## 🛠️ Setup

### ☁️ Kaggle / Colab
- Enable Internet + GPU  
- Run notebook cells  

### 💻 Local Setup

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

