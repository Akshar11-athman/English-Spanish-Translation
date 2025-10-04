English-to-Spanish Translation using Deep Learning

🔹 Project Description

This project focuses on Neural Machine Translation (NMT) from English to Spanish.
We implemented and compared classical recurrent models (RNN, LSTM, GRU) with a modern Transformer-based model (BERT / MarianMT).

The main goal is to understand how traditional sequence models differ from advanced pretrained Transformers in terms of translation accuracy.

🔹 Dataset

Source: Kaggle English–Spanish parallel dataset

Size: ~20,000 sentence pairs (subset used for training due to compute limits)

Preprocessing:

Text cleaning

Tokenization (word → integer IDs)

Padding to fixed sequence length (20 tokens)

Train/Test split (80/20)

🔹 Models Implemented

RNN – Simple sequential model

LSTM – Handles long-term dependencies

GRU – Lightweight LSTM alternative

BERT Transformer (MarianMT) – Pretrained state-of-the-art translation model

🔹 Training Setup

Frameworks: TensorFlow/Keras, HuggingFace Transformers

Optimizer: Adam

Loss: Sparse Categorical Cross-Entropy

Epochs: 3

Batch size: 64

🔹 Results

Evaluation Metric: BLEU Score

Model	BLEU Score
RNN	20.56
LSTM	17.29
GRU	9.29
BERT (MarianMT)	41.11

📊 BERT significantly outperforms recurrent models.

🔹 Example Translations

EN: Hello → ES: Hola

EN: Good morning → ES: Buenos días

EN: What is your name? → ES: ¿Cómo te llamas?

EN: How are you?

Ground Truth: ¿Cómo estás?

Predicted (GRU): ...

Predicted (BERT): ¿Cómo estás?

🔹 Future Work

Train on larger datasets

Apply beam search decoding

Use multilingual pretrained models (mBART, mT5)

Deploy as a web app or API

🔹 References

Kaggle English-Spanish Dataset

HuggingFace MarianMT

TensorFlow/Keras

SacreBLEU Toolkit
