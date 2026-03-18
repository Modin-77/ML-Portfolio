# Named Entity Recognition (NER) for News Articles

This project implements a specialized NLP pipeline to identify and categorize entities (People, Organizations, Locations) within journalistic text. It compares traditional statistical models against state-of-the-art Deep Learning architectures.

## Objectives
* **Domain Specificity:** Tailored for the unique vocabulary and structure of news reporting.
* **Hybrid Modeling:** Benchmarked **Naïve Bayes** and **HMM** against **BiLSTM** and **BERT**.
* **Information Extraction:** Designed to assist in automated news summarization and event tracking.

## Model Architecture
The core of this project focuses on the **BERT-BiLSTM** hybrid:
1. **BERT Embeddings:** To capture deep contextual meaning of words.
2. **BiLSTM Layer:** To process the sequence dependencies from both directions.
3. **Softmax Output:** For final entity classification (e.g., B-PER, I-ORG).

## Tech Stack
* **Transformers:** Hugging Face `transformers` library (BERT).
* **Deep Learning:** TensorFlow/Keras.
* **NLP Tools:** Spacy, NLTK.
* **Data:** CoNLL-2003 / Reuters News Dataset.

## 📄 Documentation
The full technical proposal and methodology can be found in the `NER_Project_Proposal.pdf` included in this folder.
