#  GRU + Word2Vec Model

##  Overview
This model uses a GRU network combined with pretrained Word2Vec embeddings from Gensim.

---

##  Architecture
- Embedding Layer (Word2Vec pretrained, 100 dim)
- GRU (96 units)
- Dense (64, ReLU)
- Dropout (0.5)
- Output (Sigmoid)

---

##  Techniques Applied
- Pretrained Word2Vec embeddings
- Tokenization & padding
- Dropout regularization
- Early stopping
- Learning rate scheduling
- Gradient clipping

---

##  Results
See `GRU_Word2VecResults.txt`
