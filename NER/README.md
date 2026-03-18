# 📄 Smart Resume Parser (BERT-BiLSTM NER)

A deep learning-based Information Extraction (IE) system designed to automate resume parsing. This project utilizes state-of-the-art Transformer embeddings and Bi-Directional LSTMs to identify key entities like Candidate Names, Organizations, and Locations.

## 🚀 The Big Picture
* **Core Architecture:** BERT (Contextual Embeddings) + BiLSTM (Sequence Learning).
* **Dataset:** Trained on CoNLL-2003 (standard benchmark for NER).
* **Deployment:** Integrated with a **Gradio Web App** for real-time text processing and colored entity visualization.

## 🧠 Model Architecture
The pipeline follows a sophisticated hybrid approach:
1. **BERT (bert-base-cased):** Generates 768-dimension contextual vectors for each token.
2. **Label Alignment:** Custom preprocessing to align BERT's subword tokens with word-level entity labels.
3. **BiLSTM Layer:** Processes sequences forward and backward to capture global context.
4. **TimeDistributed Dense:** A Softmax layer predicts specific tags (PER, LOC, ORG, MISC) for every token.



## 📊 Performance Results
The model achieved an **Overall F1-score of ~87%** after only 3 epochs of training.

| Entity | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: |
| **Person (PER)** | **0.96** | **0.93** | **0.95** |
| **Location (LOC)** | 0.87 | 0.88 | 0.88 |
| **Organization (ORG)** | 0.82 | 0.84 | 0.83 |

### Key Insight
The model is exceptionally strong at identifying **Candidate Names (95% F1)**, making it highly effective for the initial stages of automated recruitment filtering.

## 🛠️ Tech Stack
* **Models:** BERT, BiLSTM, TensorFlow/Keras.
* **Tools:** Hugging Face Transformers, Gradio (UI), Seqeval (Evaluation).
* **Data:** CoNLL-2003 via `datasets` library.

## 🌐 How it Works (UI)
The system takes raw resume text as input and outputs an HTML-formatted string where:
* <span style="color:red">**Names**</span> are highlighted in Red.
* <span style="color:blue">**Organizations**</span> are highlighted in Blue.
* <span style="color:green">**Locations**</span> are highlighted in Green.
