# 📝 Next Word Prediction using LSTM

A Deep Learning-based Next Word Prediction model built using TensorFlow and Keras. The model is trained on a text corpus to learn language patterns and predict the most probable next word for a given input sequence.

---

## 📌 Project Overview

This project demonstrates the implementation of a Recurrent Neural Network (RNN) using Long Short-Term Memory (LSTM) layers for language modeling. Given an input phrase, the model predicts the next likely word based on patterns learned during training.

Example:

Input:
```
To be or not
```

Output:
```
to
```

---

## 🚀 Features

- Text preprocessing and tokenization
- Sequence generation for supervised learning
- Padding of variable-length sequences
- LSTM-based language model
- Next-word prediction
- Easy-to-use prediction function
- Supports custom text datasets

---

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- NLTK
- Jupyter Notebook

---

## 📂 Project Structure

```
Next-Word-Prediction/
│
├── data/
│   └── corpus.txt
│
├── notebooks/
│   └── Next_Word_Prediction.ipynb
│
├── model/
│   └── next_word_model.keras
│
├── tokenizer/
│   └── tokenizer.pkl
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Workflow

### 1. Data Collection

Load a text corpus containing sentences or paragraphs.

### 2. Text Preprocessing

- Convert text to lowercase
- Remove unnecessary characters
- Tokenize words
- Build vocabulary

### 3. Sequence Generation

Generate n-gram sequences.

Example:

```
I love
I love deep
I love deep learning
```

### 4. Padding

Pad all sequences to the same length.

### 5. Model Building

Architecture:

```
Embedding Layer
        ↓
LSTM (150 units)
        ↓
Dropout
        ↓
LSTM (100 units)
        ↓
Dense (Softmax)
```

### 6. Training

- Loss Function: Categorical Crossentropy
- Optimizer: Adam
- Metric: Accuracy

### 7. Prediction

Input a sentence, and the trained model predicts the most probable next word.

---

## 🧠 Model Architecture

| Layer | Output |
|--------|---------|
| Embedding | Word Embeddings |
| LSTM (150) | Sequence Learning |
| Dropout | Regularization |
| LSTM (100) | Context Learning |
| Dense | Vocabulary Probability Distribution |

---

## 📈 Sample Prediction

```python
input_text = "To be or not"

next_word = predict_next_word(
    model,
    tokenizer,
    input_text,
    max_sequence_len
)

print(next_word)
```

Output:

```
to
```

---

## 📊 Training

Compile the model:

```python
model.compile(
    loss='categorical_crossentropy',
    optimizer='adam',
    metrics=['accuracy']
)
```

Train:

```python
history = model.fit(
    xs,
    ys,
    epochs=100,
    batch_size=64,
    validation_split=0.2
)
```

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/Next-Word-Prediction.git
```

Navigate to the project:

```bash
cd Next-Word-Prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```

---

## 📋 Requirements

```
tensorflow
numpy
pandas
nltk
scikit-learn
matplotlib
jupyter
```

---

## 🔮 Future Improvements

- Replace LSTM with Transformer architecture
- Beam Search decoding
- Top-k and Top-p sampling
- GRU implementation
- Attention Mechanism
- Train on larger datasets
- Deploy using Flask/FastAPI
- Build a Streamlit web application
- Add interactive text generation

---

## 📚 Learning Outcomes

This project covers:

- Natural Language Processing (NLP)
- Text Tokenization
- Sequence Padding
- Word Embeddings
- Language Modeling
- LSTM Networks
- Deep Learning with TensorFlow
- Sequence Prediction



