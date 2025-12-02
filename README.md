# From Sequences to Transformers: LSTM vs. BERT for Sentiment Analysis

[![Paper Status](https://img.shields.io/badge/Status-Published-success)](https://journals.cfrit.com/index.php/ijisct/article/view/139)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)

##  Abstract
This repository contains the official implementation of the research paper **"From Sequences to Transformers: LSTM and BERT Powering Next-Gen Sentiment Analysis"**.

Sentiment analysis is a cornerstone of modern customer feedback analysis. This study provides a rigorous, controlled comparison between **Long Short-Term Memory (LSTM)** networks and **Bidirectional Encoder Representations from Transformers (BERT)** on the Amazon Fine Food Reviews dataset (50,000 samples).

While BERT achieves superior accuracy by capturing bidirectional context and sarcasm, LSTM remains a viable candidate for resource-constrained environments due to its inference speed and lower memory footprint.

> ** Read the Official Paper:** [View on Journal Website](https://journals.cfrit.com/index.php/ijisct/article/view/139)

##  Key Results
We evaluated both models on a held-out test set of 5,000 samples. BERT consistently outperformed LSTM across all major metrics.

| Metric | LSTM | BERT (Fine-Tuned) | Difference |
|--------|------|-------------------|------------|
| **Accuracy** | 84.2% | **88.2%** | +4.0% |
| **F1-Score** | 0.843 | **0.883** | +0.040 |
| **ROC-AUC** | 0.901 | **0.942** | +0.041 |
| **MCC** | 0.680 | **0.764** | +0.084 |

*Data sourced from Table 2 of the original paper.*

##  Model Architecture
We compared two distinct architectural paradigms:
1.  **LSTM (Sequential):** Processes text step-by-step. Efficient but struggles with long-range dependencies and sarcasm .
2.  **BERT (Transformer):** Uses self-attention to process the entire sequence at once. Excellent at understanding context, negation, and irony .

##  The Trade-off: Accuracy vs. Efficiency
A key finding of this research is the trade-off between performance and cost. While BERT is more accurate, LSTM is significantly faster and requires less memory, making it suitable for edge deployment.

*(See the Interactive Radar Chart on our [Project Website](https://Muhammad-Shahan.github.io/BERT-vs-LSTM-Sentiment/) for a visual breakdown).*

