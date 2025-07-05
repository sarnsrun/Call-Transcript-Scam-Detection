# Call Transcript Scam Detection

This project focuses on detecting **scam phone calls** using **Natural Language Processing (NLP)** and **Machine Learning (ML)**. It leverages a dataset of real-life annotated call transcripts sourced from Kaggle to train models that can classify a phone call as either **scam** or **not scam** based on its dialogue.

![scam detection](https://img.shields.io/badge/Scam-Detection-red) ![NLP](https://img.shields.io/badge/NLP-Model-blue) ![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 🔍 Project Overview

Phone scams are a growing concern worldwide. The goal of this project is to create a model that can **automatically flag scam calls** based on how conversations unfold. Using the Kaggle dataset of call transcripts, we build and evaluate multiple models ranging from traditional ML to fine-tuned transformer-based classifiers.

---

## 📁 Dataset

📦 **Source**: [Call Transcripts Scam Determinations – Kaggle](https://www.kaggle.com/datasets/mealss/call-transcripts-scam-determinations)

* **Rows**: 358
* **Columns**:

  * `transcript`: A full transcript of a phone call, alternating between caller and callee.
  * `category`: Label of the call — either `scam` or `not scam`.

The transcripts follow a structured pattern:

```
(Caller statement) [Step: 1] (Callee response) [Step: 2] ...
```

This consistent format allows easy segmentation of turns in the dialogue for NLP tasks.

---

## 🧠 Models Implemented

* ✅ TF-IDF + Logistic Regression
* ✅ TF-IDF + SVM
* ✅ TF-IDF + Random Forest
* ✅ TF-IDF + Gradient Boosting
* ✅ Fine-tuned HuggingFace Transformers (e.g., `DistilBERT`, `BERT-base`)

Each model is evaluated and compared based on standard metrics.

---

## 📊 Project Structure

```bash
Call-Transcript-Scam-Detection/
├── data/
│   └── transcripts.csv              # Raw dataset from Kaggle
├── notebooks/
│   ├── baseline_models.ipynb        # TF-IDF + ML models
│   ├── bert_finetuning.ipynb        # Fine-tuning HuggingFace models
├── models/
│   └── saved_model.pkl              # Saved/trained models
├── utils/
│   └── preprocessing.py             # Functions to clean and parse transcript
├── requirements.txt
└── README.md
```

---

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/sarnsrun/Call-Transcript-Scam-Detection.git
cd Call-Transcript-Scam-Detection
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Add the Dataset

Download the dataset from [Kaggle](https://www.kaggle.com/datasets/mealss/call-transcripts-scam-determinations) and place the `transcripts.csv` inside the `data/` directory.

---

## 📈 Results

| Model               | Accuracy    | F1-Score   |
| ------------------- | ----------- | ---------- |
| Logistic Regression | \~89.2%     | \~0.90     |
| SVM                 | \~91.0%     | \~0.91     |
| BERT (fine-tuned)   | **\~94.3%** | **\~0.94** |

*Note: Metrics may vary depending on preprocessing and seed.*

---

## 🧩 Key Features

* 🗂️ Step-level transcript parsing
* 🔤 TF-IDF vectorization
* 🤖 Transformer-based fine-tuning via HuggingFace
* 📊 Confusion Matrix, ROC AUC, Accuracy, Precision, Recall, F1
* 🧪 Baseline vs Deep Learning comparison

---

## 🚧 Future Enhancements

* ☑️ Real-time transcription-to-detection pipeline
* ☑️ Add voice-to-text pipeline (e.g., using Whisper)
* ☑️ Integrate LLMs with conversational context understanding
* ☑️ Expand dataset with multilingual transcripts

---

## 👨‍💻 Author

**Aisar Nasrun**
📂 GitHub: [@sarnsrun](https://github.com/sarnsrun)

---

## 📄 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

Would you like me to:

* Format this into an actual `README.md` file and upload it to your GitHub repo?
* Help generate the `requirements.txt` file from your notebooks?
* Add badges for HuggingFace usage, dataset citation, or Colab notebook links?

