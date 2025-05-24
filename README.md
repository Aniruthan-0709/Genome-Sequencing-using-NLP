# 🧬 Genome Sequencing Using NLP

A machine learning and deep learning-based project for promoter region classification in genomic DNA sequences using natural language processing (NLP) techniques. This project demonstrates how DNA sequences can be treated as biological text to improve classification accuracy for genomic research.

## 📌 Project Highlights

- **Problem:** Predict whether a DNA sequence is a promoter or non-promoter region.
- **Dataset:** Drosophila Melanogaster genome (22,598 labeled sequences in FASTA format)
- **Techniques:**
  - k-mer tokenization (similar to NLP n-grams)
  - TF-IDF vectorization
  - One-hot encoding
  - Classical ML models: Random Forest, LightGBM, Naive Bayes, Logistic Regression
  - Deep Learning models: LSTM, BiLSTM, CNN
  - Ensemble methods: Voting and Stacking classifiers
- **Best Result:** CNN model with one-hot encoded k-mers (k=6) achieved **91.3% accuracy**

---

## 🧠 Motivation

Promoter region identification is crucial for understanding gene expression and biological functions. Traditional techniques like DNase footprinting and ChIP-seq are accurate but costly and time-intensive. By leveraging NLP techniques, we aim to provide a scalable, automated solution that transforms raw genome data into structured features for classification.

---

## 📊 Data Overview

- **Source:** [IEEE DataPort - Drosophila Melanogaster Genome](https://dx.doi.org/10.5072/FK2GT5M94X)
- **Format:** FASTA
- **Classes:** Promoter (1), Non-Promoter (0)
- **Size:** 22,598 sequences (balanced)

---

## 🧪 Techniques & Models

### 🧬 Preprocessing
- Uppercasing, unknown nucleotide filtering
- Sequence length standardization
- k-mer generation (k=5–6)
- Label mapping
- Duplicate removal

### 🔍 Feature Engineering
- TF-IDF on k-mers
- One-hot encoding for CNN, LSTM, BiLSTM

### 🤖 Models Implemented
| Model                     | Accuracy (%) |
|--------------------------|--------------|
| Random Forest + TF-IDF   | 72.2         |
| LightGBM + TF-IDF        | 78.4         |
| Naive Bayes + TF-IDF     | 74.3         |
| Logistic Regression      | 78.2         |
| LSTM                     | 69.1         |
| BiLSTM                   | 67.3         |
| **CNN**                  | **91.3**     |

---

## 🖼️ Visualizations

- Class balance bar chart
- Nucleotide frequency heatmaps
- Sequence length distribution
- EDA on promoter vs. non-promoter patterns

---

## 🔮 Future Enhancements

- Integrate transformer models like **DNABERT**
- Include biological metadata (e.g., gene location, conservation)
- Expand to **multi-class classification**: enhancers, silencers, exons

---

## Acknowledgements

- This work is inspired by state-of-the-art genomic classification models and was supported by coursework at Northeastern University.
