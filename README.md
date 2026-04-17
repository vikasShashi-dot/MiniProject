# MiniProject
# 🧠 Mental Health Detection using NLP & Machine Learning

## 🚀 Overview

This project is an **end-to-end Natural Language Processing (NLP) system** designed to detect mental health conditions from textual data.

It combines:

* Traditional Machine Learning models
* Transformer-based deep learning (DistilBERT)

The system classifies text into:

* **Binary Classification**: Suicidal vs Non-Suicidal
* **Multiclass Classification**: Anxiety, Depression, Suicidal Ideation, Not Suicidal

---

## 🎯 Objectives

* Build a robust NLP pipeline for mental health detection
* Compare traditional ML models vs transformer models
* Handle real-world noisy text data
* Deploy a usable interface for real-time predictions

---

## 🏗️ Project Structure

```
project/
│
├── data/
│   ├── raw/              # Original datasets
│   └── processed/        # Cleaned & split data
│
├── models/               # Saved trained models
├── results/              # Predictions & outputs
├── plots/                # Visualizations
│
└── main_project.py       # Complete pipeline
```

---

## ⚙️ Tech Stack & Why It Was Used

### 🔹 Programming Language

* **Python**

  * Industry standard for ML/NLP
  * Rich ecosystem of libraries

---

### 🔹 Data Handling & Processing

* **Pandas**

  * Used for structured data manipulation
  * Efficient handling of datasets

* **NumPy**

  * Fast numerical computations
  * Supports vectorized operations

---

### 🔹 Natural Language Processing

* **NLTK (Natural Language Toolkit)**

  * Tokenization (splitting text into words)
  * Stopword removal
  * Lemmatization (word normalization)

👉 **Why used?**

* Prepares raw text for machine learning
* Reduces noise and improves model performance

---

### 🔹 Machine Learning (Baseline Models)

* **Scikit-learn**

  * Logistic Regression
  * Naive Bayes
  * Support Vector Machine (SVM)
  * Random Forest

👉 **Why used?**

* Provides strong baseline models
* Fast to train and interpret
* Helps compare with deep learning models

---

### 🔹 Feature Engineering

* **TF-IDF Vectorizer**

  * Converts text → numerical vectors
  * Captures word importance

👉 **Why used?**

* Essential for traditional ML models
* Lightweight and efficient

---

### 🔹 Deep Learning

* **PyTorch**

  * Backend for neural networks
  * GPU acceleration support

👉 **Why used?**

* Flexible and widely used in research/industry

---

### 🔹 Transformer Models

* **DistilBERT (from Hugging Face Transformers)**

👉 **Why used?**

* Pretrained language model
* Captures **context and semantics**
* Faster and smaller than BERT (~40% lighter)
* High performance on text classification

---

### 🔹 Model Training Utilities

* **Hugging Face Trainer API**

  * Handles training loops
  * Evaluation
  * Logging

👉 **Why used?**

* Simplifies training process
* Reduces boilerplate code

---

### 🔹 Visualization

* **Matplotlib & Seaborn**

  * Plots (class distribution, confusion matrix)

👉 **Why used?**

* Helps understand data and model performance

---

### 🔹 Deployment / Interface

* **Gradio**

  * Interactive web UI

👉 **Why used?**

* Quickly deploy ML models
* Allows real-time text input and predictions

---

### 🔹 Model Persistence

* **Pickle**

  * Save trained models and vectorizers

👉 **Why used?**

* Enables reuse without retraining

---

## 🔄 Pipeline Explanation

### 1. Data Collection

* Dataset downloaded from Kaggle
* Fallback synthetic dataset for reliability

---

### 2. Data Preprocessing

Steps:

* Lowercasing
* Removing URLs & noise
* Tokenization
* Lemmatization

⚠️ Important:

* **Negation words (e.g., “not”, “never”) were preserved**
* Critical for mental health context

---

### 3. Data Splitting

* Train (70%)
* Validation (15%)
* Test (15%)

👉 Stratified split ensures balanced classes

---

### 4. Baseline Models

* TF-IDF + ML models trained
* Performance evaluated using F1-score

---

### 5. Transformer Model

* Fine-tuned DistilBERT
* Input:

  * Tokenized text
  * Attention masks
* Output:

  * Class probabilities

---

### 6. Evaluation Metrics

* Accuracy
* Precision
* Recall
* **F1-score (primary metric)**

👉 F1-score is critical for imbalanced datasets

---

### 7. Error Analysis

* Identified:

  * False positives
  * False negatives
* Helps improve model reliability

---

### 8. Deployment

* Built interactive UI using Gradio
* Supports:

  * Real-time predictions
  * Confidence scores

---

## 📊 Results

* Transformer model outperformed traditional ML models
* Better contextual understanding
* Improved classification accuracy and F1-score

---

## 🧠 Key Learnings

* Context matters in NLP → transformers outperform TF-IDF
* Preprocessing decisions (like keeping negations) are critical
* Baselines are important before deep learning
* Error analysis is essential for real-world ML systems

---

## 🚀 How to Run

```bash
# Install dependencies
pip install torch transformers scikit-learn pandas numpy nltk gradio

# Run project
python main_project.py
```

---

## 💡 Future Improvements

* Deploy using FastAPI (REST API)
* Use larger datasets
* Add real-time monitoring
* Experiment with advanced models (RoBERTa, BERT-large)

---

## 👨‍💻 Author

**Vikas Shashi**
Computer Science Engineering Student

---

## ⚠️ Disclaimer

This project is for educational purposes only and is **not a substitute for professional mental health diagnosis**.

---
