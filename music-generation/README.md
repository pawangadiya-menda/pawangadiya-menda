# 🎵 Music Generation with LSTM

A hands-on PyTorch project for generating music with a character-level LSTM in Google Colab.

## Project overview

This notebook learns patterns from Irish folk songs represented in **ABC music notation**.

```text
ABC notation
   ↓
Characters → integer IDs
   ↓
Input / target sequences
   ↓
Embedding
   ↓
LSTM
   ↓
Linear
   ↓
Next-character logits
   ↓
Cross-entropy loss
   ↓
Backpropagation + Adam
   ↓
Trained LSTM
   ↓
Autoregressive generation
   ↓
Generated ABC music
   ↓
Optional MIDI rendering
```

## What you will learn

- Character-level sequence modelling
- PyTorch `Embedding`, `LSTM`, and `Linear`
- Next-character prediction
- Cross-entropy loss
- Backpropagation and Adam
- Autoregressive generation
- Temperature-based sampling
- Optional MIDI rendering with Music21

## Notebook

[**Open the notebook**](Music_Generation_LSTM_Colab.ipynb)

The notebook is designed for **Google Colab** and uses GPU acceleration when available.

## Dataset

The notebook downloads the official MIT Introduction to Deep Learning Irish folk music dataset in ABC notation:

https://raw.githubusercontent.com/MITDeepLearning/introtodeeplearning/master/mitdeeplearning/data/irish.abc

## Key concept

The network is not directly predicting raw audio. It learns:

**Given the characters seen so far, what character is likely to come next?**

That makes this a useful bridge to understanding sequence models and the next-token prediction idea used in modern language models.

## Repository structure

```text
music-generation/
├── Music_Generation_LSTM_Colab.ipynb
└── README.md
```

## Suggested experiments

1. Increase training iterations.
2. Change sequence length and batch size.
3. Experiment with temperature.
4. Improve song extraction and ABC validity.
5. Experiment with richer symbolic music representations.

---

Part of my hands-on AI/ML learning journey, combining technical implementation with product thinking.
