# BiLSTM Model

##  Overview
This model uses a Bidirectional LSTM to capture context in both directions.

---

##  Architecture
- Embedding Layer (20,000 vocab, 100 dim)
- Bidirectional LSTM (64 units)
- Dense (64, ReLU)
- Dropout (0.5)
- Output (Sigmoid)

---

##  Techniques Applied
- Tokenization & padding
- Bidirectional learning
- Dropout
- Early stopping
- Gradient clipping
- Learning rate scheduling

---

##  Results
See `LSTMResults.txt`
