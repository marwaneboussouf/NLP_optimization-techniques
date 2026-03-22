#  1D CNN Model

##  Overview
This model uses a Convolutional Neural Network for sentiment classification.

---

##  Architecture
- Embedding Layer (20,000 vocab, 100 dim)
- Conv1D (128 filters, kernel size = 5)
- Global Max Pooling
- Dense (64, ReLU)
- Dropout (0.5)
- Output (Sigmoid)

---

##  Techniques Applied
- Tokenization & padding (length = 250)
- Dropout regularization
- Early stopping
- Learning rate scheduling
- Gradient clipping

---

##  Results
See `CNNresults.txt`
