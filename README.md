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

* ✅ LSTM + Logistic Regression
* ✅ LSTM + SVM
* ✅ LSTM + Random Forest
* ✅ LSTM + Gradient Boosting
  
Each model is evaluated and compared based on standard metrics.

---

## 📊 Project Structure

```bash
Call-Transcript-Scam-Detection/
└── BETTER30.csv              # Raw dataset from Kaggle
└── call_transcript_cleaned.csv
├── LSTM.ipynb
└── data_preprocessing.py             # Functions to clean and parse transcript
└── README.md
└── LICENSE
```

## 📈 Results

| Model                       | Accuracy     | F1-Score    |
| --------------------------- | ------------ | ----------- |
| LSTM + Gradient Boosting    | \~98.00%     | \~0.985     |
| LSTM + SVM                  | **\~98.40%**     | **\~0.988**     |
| LSTM + Random Forest        | \~98.00% | \~0.982 |
| LSTM + Logistic Regression  | **\~98.40%** | **\~0.988** |

*Note: Metrics may vary depending on preprocessing and seed.*

---

## 🧩 Key Features

* 🗂️ Data Handling & Exploration
* 🔤 Text Preprocessing
* 🤖 Model Architecture
* 🧠 Advanced Techniques (Stacking)
* 🧪 Evaluation Metrics (Accuracy, Confusion Matrix, Precision, Recall, F1-Score) 
---

## 🚧 Future Enhancements

* ☑️ Real-time transcription-to-detection pipeline
* ☑️ Add voice-to-text pipeline (e.g., using Whisper)
* ☑️ Integrate LLMs with conversational context understanding

---

## 👨‍💻 Author

**Aisar Nasrun**
📂 GitHub: [@sarnsrun](https://github.com/sarnsrun)

---

## 📄 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

