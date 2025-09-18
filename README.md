# Petition-Classification-with-Deep-Learning-and-Gradient-Boosting
Author: **Sara Hodaei**  

## Project Overview

This project explores how natural language processing (NLP) and machine learning can be used to analyze petitions submitted to the UK government. Two complementary tasks are addressed:

1. **Petition Topic Classification**  
   A deep learning model based on **Bidirectional LSTMs with FastText embeddings** is trained to predict the thematic category of a petition from its text. Several variants are explored, including attention mechanisms and class-weighted training.

2. **Petition Importance Prediction**  
   A lightweight **XGBoost classifier** is developed to identify whether a petition should be considered *important*. The model is optimised for **recall** to ensure no high-value petitions are missed, even at the cost of lower precision.  

Together, these approaches show how text analytics and machine learning can support large-scale policy and citizen engagement systems.

---

## Results

- **Topic Classification (BiLSTM + FastText)**  
  - Best model achieved **Accuracy = 86.7%**, **Macro F1 = 0.836**, **AUC = 0.99**.  
  - Attention improved interpretability, though not overall accuracy.  
  - Macro F1 was found to be the fairest metric given class imbalance.

- **Importance Classification (XGBoost)**  
  - Achieved **Recall = 1.00** for the “important” class.  
  - Precision trade-offs were acceptable for decision-support use.  
  - Shows potential as a **filtering tool** to highlight petitions requiring human review.  

---

## Repository Structure

```text
petition-classification-ml/
│
├── README.md                 → Project overview
├── LICENSE                   → MIT License
├── requirements.txt           → Dependencies
│
├── report/
│   └── Petition_Classification_Report.pdf
│
└── notebooks/
    └── petition_classification.ipynb
