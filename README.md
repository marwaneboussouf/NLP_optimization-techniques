#  IMDB Sentiment Analysis – Assignment 2 (Deep Learning Models)

##  Overview
This project improves upon **Assignment 1**, where sentiment classification was performed using handcrafted features.

In this assignment, we use **deep learning models** to process full text reviews instead of limited features, leading to better performance.

---

##  Project Structure

```
assignment2_imdb_models/
│
├── cnn/
│   ├── best_model.pt
│   ├── results.txt
│   ├── README.md
│   ├── history.csv
│   └── confusion_matrix.csv
│
├── lstm/
├── gru/
│
└── all_model_results.csv
```

---

##  Models Implemented

### 1️ 1D Convolutional Neural Network (CNN)
**Architecture:**
- Embedding Layer  
- Conv1D (128 filters, kernel size = 5)  
- Global Max Pooling  
- Dense Layer (64 units)  
- Dropout (0.5)  
- Output Layer (Sigmoid)  

**Purpose:**  
Captures local text patterns (like n-grams) efficiently.

---

### 2️ Bidirectional LSTM (BiLSTM)
**Architecture:**
- Embedding Layer  
- Bidirectional LSTM (hidden size = 64)  
- Dense Layer (64 units)  
- Dropout (0.5)  
- Output Layer (Sigmoid)  

**Purpose:**  
Captures long-term dependencies and word order in sequences.

---

### 3️ GRU (Gated Recurrent Unit)
**Architecture:**
- Embedding Layer  
- GRU Layer (hidden size = 96)  
- Dense Layer (64 units)  
- Dropout (0.5)  
- Output Layer (Sigmoid)  

**Purpose:**  
Faster alternative to LSTM with fewer parameters.

---

##  Techniques Applied

###  Data Processing
- Tokenization of text  
- Vocabulary limited to top 20,000 words  
- Sequence padding to length = 250  

---
###  Optimization Techniques
- Early Stopping  
- Learning Rate Scheduling  
- Gradient Clipping  
- Dropout Regularization  
- Weight Decay (L2)  

---

###  Training Details
- Loss Function: Binary Cross Entropy  
- Optimizer: Adam  
- Batch Size: 64  
- Epochs: up to 10 (with early stopping)  

---

##  Evaluation

Each model is evaluated using:
- Accuracy  
- Loss  
- Confusion Matrix  

Results are saved in:
```
results.txt
confusion_matrix.csv
```

Global comparison:
```
all_model_results.csv
```

---

##  Improvements Over Assignment 1

| Aspect | Assignment 1 | Assignment 2 |
|--------|-------------|-------------|
| Input | 6 handcrafted features | Full text sequences |
| Models | MLP | CNN, LSTM, GRU |
| Feature Learning | Manual | Automatic |
| Performance | Limited | Improved |

---

##  How to Run

1. Upload notebook to Google Colab  
2. Run all cells  
3. Wait for training  
4. Check outputs in:
```
assignment2_imdb_models/
```

---

##  Notes
- No additional installations required (Colab compatible)  
- Dataset: IMDB movie reviews (binary sentiment classification)  
- Optional speed-up:
```python
SAMPLE_SIZE = 10000
```

---

## Author
marwane BOUSSOUF  
Computer Science Student – AI  

---

## ✅ Summary
This project demonstrates how deep learning:
- Learns features automatically from text  
- Improves classification performance  
- Scales better than traditional ML  
