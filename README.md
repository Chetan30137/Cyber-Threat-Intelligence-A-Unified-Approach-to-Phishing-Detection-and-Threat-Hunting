# Cyber Threat Intelligence: A Unified Approach to Phishing Detection and Threat Hunting

An integrated machine-learning and deep-learning project for identifying phishing emails, detecting malicious URLs, and classifying suspicious network activity for threat-hunting use cases.

The project brings together three complementary detection workflows:

- **Email Phishing Detection** using a fine-tuned DistilBERT text classifier.
- **URL Phishing Detection** using LightGBM, CatBoost, and TabNet.
- **Network Threat Hunting** using Graph Convolutional Networks (GCNs), TabNet, Autoencoders, and transformer-based classification.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Project Objectives](#project-objectives)
- [Project Modules](#project-modules)
- [Technology Stack](#technology-stack)
- [Repository Structure](#repository-structure)
- [Datasets](#datasets)
- [Installation](#installation)
- [Running the Project](#running-the-project)
- [Model Evaluation](#model-evaluation)
- [Limitations and Future Enhancements](#limitations-and-future-enhancements)
- [Responsible Use](#responsible-use)
- [Author](#author)

---

## 🔍 Overview

Phishing and network-based attacks are major cybersecurity threats. Phishing emails manipulate users into revealing sensitive information, malicious URLs redirect users to fraudulent websites, and suspicious network traffic may indicate scanning, exploitation, or other malicious activity.

This project presents a unified, data-driven approach to these cybersecurity challenges.

It combines Natural Language Processing (NLP), Machine Learning (ML), and Deep Learning (DL) techniques to develop detection models for:

1. Phishing email identification.
2. Malicious URL classification.
3. Network threat detection and hunting.

Each module is implemented independently using Jupyter Notebooks, allowing individual model training, experimentation, and evaluation.

## 🎯 Project Objectives

- Detect phishing emails and distinguish them from legitimate emails.
- Identify malicious URLs using supervised machine-learning algorithms.
- Analyse network traffic and identify suspicious or attack-related activities.
- Apply transformer-based NLP models for cybersecurity text classification.
- Explore graph-based learning for network threat detection.
- Compare different ML and DL approaches using standard evaluation metrics.
- Develop a foundation for an integrated Cyber Threat Intelligence platform.

---

## 🛡️ Project Modules

### 1. Email Phishing Detection

**Notebook:** `Phishing_EMAIL_FINAL.ipynb`

This module uses **DistilBERT**, a transformer-based language model, to classify emails as phishing or legitimate.

**Methodology:**

1. Load the email dataset.
2. Extract email text and corresponding labels.
3. Convert labels into binary classes:
   - `0` – Safe Email
   - `1` – Phishing Email
4. Split the dataset into training and testing sets.
5. Tokenize email content using the DistilBERT tokenizer.
6. Fine-tune the pretrained `distilbert-base-uncased` model.
7. Evaluate the trained model.
8. Save the model weights and tokenizer for future inference.

**Model Used:**

- DistilBERT (`distilbert-base-uncased`)

**Evaluation Metrics:**

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- ROC Curve
- AUC

### 2. URL Phishing Detection

**Notebook:** `Phishing_URL.ipynb`

This module focuses on detecting phishing URLs using supervised machine-learning and deep-learning algorithms.

**Algorithms Implemented:**

- LightGBM
- CatBoost
- TabNet
- Optuna for hyperparameter optimization

**Methodology:**

1. Load the phishing URL dataset.
2. Perform data preprocessing and feature preparation.
3. Separate input features and target labels.
4. Split the dataset into training and testing sets.
5. Train multiple classification models.
6. Perform hyperparameter optimization using Optuna.
7. Compare model performance.
8. Evaluate predictions using classification metrics.

**Evaluation Metrics:**

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- ROC Curve
- AUC

### 3. Network Threat Hunting

**Notebook:** `Threat_Hunting.ipynb`

This module focuses on analysing network traffic and identifying suspicious or malicious activities through machine-learning and deep-learning techniques.

**Approaches Implemented:**

**Graph Convolutional Network (GCN)**

- Uses PyTorch Geometric and GCNConv.
- Explores graph-based representation learning for network traffic.
- Learns patterns from network-related features.

**TabNet**

- Uses attention-based deep learning for tabular network traffic classification.
- Identifies relevant features for threat classification.

**Autoencoder**

- Explores unsupervised representation learning.
- Learns compressed representations of network features.

**Transformer-Based Classification**

- Uses Hugging Face transformer models.
- Converts selected network attributes into text-based representations.
- Performs threat-category classification.

**Network Attributes Analysed:**

- Source IP Address
- Destination IP Address
- Source Port
- Destination Port
- Protocol
- Service
- Network Traffic Features
- Packet and Byte Counts
- Attack Labels

**Evaluation Metrics:**

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix
- ROC Curve
- AUC

---

## ⚙️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Development Environment | Jupyter Notebook |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| NLP | Hugging Face Transformers, DistilBERT |
| Deep Learning | PyTorch |
| Graph Neural Networks | PyTorch Geometric |
| Gradient Boosting | LightGBM, CatBoost |
| Tabular Deep Learning | PyTorch TabNet |
| Hyperparameter Optimization | Optuna |
| Data Visualization | Matplotlib, Seaborn |

---

## 📂 Repository Structure

```text
Cyber-Threat-Intelligence-A-Unified-Approach-to-Phishing-Detection-and-Threat-Hunting/
│
├── Phishing/
│   └── Email and URL phishing-related resources
│
├── ThreatHunting/
│   └── Network threat-hunting-related resources
│
├── Phishing_EMAIL_FINAL.ipynb
│
├── Phishing_URL.ipynb
│
├── Threat_Hunting.ipynb
│
├── .gitattributes
│
└── README.md


## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Chetan30137/Cyber-Threat-Intelligence-A-Unified-Approach-to-Phishing-Detection-and-Threat-Hunting.git
cd Cyber-Threat-Intelligence-A-Unified-Approach-to-Phishing-Detection-and-Threat-Hunting
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
pip install transformers torch
pip install lightgbm catboost pytorch-tabnet
pip install imbalanced-learn
pip install jupyter notebook
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the relevant notebook and execute the cells in sequence.

---

## Project Workflow

### Phishing Email Detection

1. Load the email dataset.
2. Perform data cleaning and preprocessing.
3. Convert email text into model-compatible input.
4. Fine-tune or evaluate the DistilBERT model.
5. Predict whether an email is phishing or legitimate.
6. Evaluate model performance using classification metrics.

### Phishing URL Detection

1. Load the URL dataset.
2. Extract and preprocess URL-related features.
3. Prepare training and testing datasets.
4. Train machine learning and deep learning models.
5. Predict whether a URL is malicious or legitimate.
6. Compare model performance using evaluation metrics.

### Network Threat Hunting

1. Load network traffic datasets.
2. Inspect and preprocess network-related information.
3. Analyze network activity for suspicious patterns.
4. Identify potentially malicious or anomalous behavior.
5. Examine results to support threat investigation.

---

## Model Evaluation

The project evaluates models using the following metrics:

| Metric | Description |
|---|---|
| Accuracy | Measures the overall percentage of correct predictions. |
| Precision | Measures how many predicted positive samples are actually positive. |
| Recall | Measures how many actual positive samples are correctly identified. |
| F1-Score | Harmonic mean of precision and recall. |
| Confusion Matrix | Shows correct and incorrect classification results. |

### Recorded Model Results

The following values were recorded in the project notebooks:

#### Phishing Email Detection

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| DistilBERT | 95.73% | 95.08% | 93.55% | 94.31% |

#### Phishing URL Detection

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| LightGBM | 97.25% | 98.44% | 95.95% | 97.18% |
| CatBoost | 94.45% | 98.13% | 90.49% | 94.15% |
| TabNet | 91.95% | 97.80% | 85.63% | 91.31% |

*Note: These are recorded experimental results. Actual performance may vary depending on dataset versions, preprocessing, training configuration, and execution environment.*

---

## Dataset Information

The project uses datasets related to phishing detection and network threat analysis.

| Dataset | Purpose |
|---|---|
| Email Dataset | Phishing and legitimate email classification. |
| URL Dataset | Malicious and legitimate URL classification. |
| IIoT Network Dataset | Network traffic analysis and threat hunting. |
| Threat Hunting Dataset | Investigation of potentially suspicious network activity. |

### Email Dataset Columns

| Column | Description |
|---|---|
| Email Text | Content of the email. |
| Email Type | Classification label, such as Phishing Email or Safe Email. |

**Important:** Dataset files may not be included in the repository because of size, licensing, or availability constraints. Update the dataset paths in the notebooks according to your local environment.

---

## Technologies Used

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Deep Learning | PyTorch |
| NLP | Hugging Face Transformers, DistilBERT |
| URL Classification | LightGBM, CatBoost, TabNet |
| Data Visualization | Matplotlib, Seaborn |
| Development Environment | Jupyter Notebook |

---

## Applications

- Identification of phishing emails.
- Detection of potentially malicious URLs.
- Support for cybersecurity threat intelligence.
- Network traffic investigation.
- Identification of suspicious network behavior.
- Assistance with security monitoring and threat hunting.

---

## Future Enhancements

- Develop a unified phishing detection interface.
- Integrate real-time email and URL analysis.
- Incorporate additional threat intelligence feeds.
- Improve network anomaly detection capabilities.
- Build an interactive cybersecurity dashboard.
- Integrate automated alert generation.
- Explore explainable AI techniques for model predictions.
- Deploy the solution as a scalable web application.

---

## Limitations

- Model performance depends on the quality and diversity of the datasets.
- Detection accuracy may vary when analyzing previously unseen phishing techniques.
- Network threat hunting results depend on the available network traffic information.
- The notebooks are primarily intended for experimentation and research.
- Predictions should be validated before making security decisions.

---

## Responsible Use

This project is developed for educational, research, and defensive cybersecurity purposes.

The system is intended to support phishing detection, threat intelligence analysis, and network threat hunting. It should only be used with datasets and network traffic that you are authorized to access and analyze.

The predictions generated by machine learning models should not be treated as definitive proof of malicious activity.

---

## Author

**Kesari Chetan Sri Reddy**

- GitHub: [Chetan30137](https://github.com/Chetan30137)
- LinkedIn: [Chetan Sri Reddy](https://www.linkedin.com/in/chetan-sri-reddy-ab854b250/)

---

## Acknowledgements

I would like to acknowledge the open-source cybersecurity, machine learning, and deep learning communities whose tools, frameworks, and research contributions supported the development of this project.

---

## License

This project is intended for academic and educational purposes. Add a suitable open-source license to the repository if you intend to distribute or reuse the project under specific licensing terms.
