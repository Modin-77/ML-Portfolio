# Cyberbullying Detection System (NLP)

This project focuses on the automated detection and categorization of cyberbullying content on Twitter using Natural Language Processing (NLP). 

## Dataset Overview
The model was trained on 47,000+ labeled tweets. The distribution across categories (Religion, Age, Ethnicity, Gender, etc.) is shown below:

![Dataset Distribution](results/Dataset%20Distribution.png)

## Performance & Results
I benchmarked multiple models to find the most accurate classifier for toxic text.

### 1. Model Comparison
The **SVM** model emerged as the most reliable for this specific task, though **CNN** and **LSTM** architectures were also explored for deep learning benchmarks.

![Model Comparison](results/Model%20Comparison.png)

### 2. Deep Learning Training (CNN & LSTM)
Below are the training accuracy and loss curves for the deep learning implementations:

| CNN Training | LSTM Training |
| :---: | :---: |
| ![CNN Plot](results/Cnn%20Training%20Plot.png) | ![LSTM Plot](results/Lstm%20Training%20Plots.png) |

### 3. Confusion Matrix
The final classification performance shows high precision in distinguishing between specific bullying types, ensuring the model doesn't just detect "toxicity" but identifies the *nature* of the abuse.

![Confusion Matrix](results/Confusion%20Matrix.png)

## 🛠️ Tech Stack
* **Models:** SVM, Naive Bayes, CNN, LSTM.
* **Libraries:** TensorFlow, Keras, Scikit-learn, NLTK.
* **Feature:** Real-time text detector function.
