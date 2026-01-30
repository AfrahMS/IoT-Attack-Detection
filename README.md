#  IoT Attack Detection using Supervised Machine Learning Techniques

This repository contains the implementation and experimental setup related to the research paper:

**“IoT Attacks Detection Using Supervised Machine Learning Techniques”**
published in *HighTech and Innovation Journal, 2024*.

The project focuses on detecting Flood DoS and RTSP brute-force attacks in IoT environments using supervised Machine Learning (ML) and Deep Learning (DL) techniques, leveraging a recent and realistic IoT traffic dataset.

---

## 📌 Abstract

The rapid growth of Internet of Things (IoT) devices has significantly increased security risks due to their limited computational resources and weak built-in defenses.
This project applies supervised ML and DL models to analyze IoT network traffic and accurately detect cyberattacks targeting IoT devices.

Two experimental scenarios are conducted using different feature sets to evaluate the impact of feature selection on detection performance. The effectiveness of the proposed approach is assessed using standard classification metrics.

---

## 🧠 Models Implemented

* Artificial Neural Network (ANN)
* Decision Tree (DT)
* Gradient Boosting (GB)
* k-Nearest Neighbors (KNN)
* Logistic Regression (LR)
* Naïve Bayes (NB)
* Support Vector Machine (SVM)
* Random Forest (RF)

Each model is evaluated under:

* Experiment 1: Six selected traffic features
* Experiment 2: Reduced feature set (three features using RFE)

---

## 🛠️ Technologies & Tools

* Python
* Scikit-learn
* TensorFlow / Keras
* CICFlowMeter
* Google Colab / Jupyter Notebook
* Grid Search with Cross-Validation
* SMOTE (Data Balancing)

---

## 📊 Dataset

* Dataset: CIC IoT Dataset 2022
* Device Analyzed: SimCam IoT device
* Attack Types:

  * Flood Denial of Service (DoS)
  * RTSP Brute-force
  * Normal traffic
* Original Format: PCAP
* Final Records: 13,315 network flows
* Extracted Features: 80+ traffic features

### ⚙️ Preprocessing Steps

* PCAP → CSV conversion using CICFlowMeter
* Label encoding (Flood, Brute-force, Normal)
* Data normalization (Min–Max scaling)
* Class imbalance handling:

  * Under-sampling
  * Over-sampling using SMOTE

---

## ⚙️ Feature Selection

Two feature selection strategies were applied:

1. Manual Feature Correlation Elimination
2. Recursive Feature Elimination (RFE)

### Feature Sets Used

* **Experiment 1 (6 features):**

  * Protocol
  * Flow IAT Max
  * Fwd Pkts/s
  * Bwd Pkts/s
  * Pkt Len Max
  * Fwd Act Data Pkts

* **Experiment 2 (3 features):**

  * Fwd Pkts/s
  * Bwd Pkts/s
  * Pkt Len Max

`Pkt Len Max` showed the highest correlation with attack behavior.

---

## 📈 Evaluation Metrics

Model performance is evaluated using:

* Accuracy
* Precision
* Recall
* F1-score

Dataset split:

* **Training:** 80%
* **Testing:** 20%

---

## 📊 Key Findings

* Gradient Boosting achieved the highest accuracy:

  * 95.94% (Experiment 1)
  * 95.28% (Experiment 2)
* Decision Tree and Random Forest showed strong and stable performance
* Feature reduction caused only minor performance degradation
* `Pkt Len Max` proved to be the most discriminative feature
* ML models effectively detected Flood DoS and RTSP brute-force attacks despite dataset imbalance

---

## 📚 Citation

If you use this work, please cite:

> Aljabri, M., Shaahid, A., Alnasser, F., Saleh, A., Alomari, D., Aboulnour, M., Al-Eidarous, W., & Althubaity, A.
> *IoT Attacks Detection Using Supervised Machine Learning Techniques.*
> HighTech and Innovation Journal, 2024.

---
