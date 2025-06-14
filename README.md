
# Flipkart Product Review Sentiment Analysis using Deep Learning

## 🧾 Overview

This project uses a **Deep Learning-based NLP model** to analyze customer reviews from Flipkart and classify them into positive or negative sentiments. The model is built using **Keras with TensorFlow backend**, showcasing how deep learning can be applied to real-world text classification problems.

---

## 🧠 Business Understanding

In e-commerce platforms like Flipkart, understanding customer sentiment is crucial for:
- Identifying product performance and customer satisfaction
- Enhancing user experience
- Flagging negative trends early
- Improving recommendations and marketing

Manual review analysis is infeasible at scale — hence, an automated sentiment classifier is highly valuable.

---

## 📊 Data Understanding

The dataset includes:
- Customer-written **review texts**
- Corresponding **star ratings** (used to infer sentiment)

### Preprocessing:
- Text normalization (lowercasing, punctuation removal)
- Stopword removal
- Tokenization and padding for LSTM input
- Label creation: binary sentiment (`positive` vs `negative`) from ratings

---

## 🤖 Modelling & Evaluation

### Deep Learning Model:
- Built using **Keras Sequential API**
- Architecture:
  - Embedding Layer
  - LSTM/GRU Layer
  - Dense Output Layer with Sigmoid activation

### Training:
- Loss Function: Binary Crossentropy
- Optimizer: Adam
- Validation Split: 20%

### Evaluation:
- Accuracy, Precision, Recall, F1-Score
- Confusion Matrix
- Visual performance plots (training vs validation loss & accuracy)

---

## 📌 Conclusion

- Achieved strong classification performance on real-world review data
- LSTM captured sequential patterns in text effectively
- Demonstrates end-to-end deep learning workflow for NLP classification

---

## ✅ Tech Stack

- Python
- Keras, TensorFlow
- NLTK, Scikit-learn
- Matplotlib, Seaborn

---
