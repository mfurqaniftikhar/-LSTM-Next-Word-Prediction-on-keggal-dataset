# 🔤 LSTM Next Word Prediction

Deep learning model for predicting the next word in a text sequence. Uses Kaggle dataset with LSTM layers to learn word patterns and dependencies.

---

## 🎯 Overview

A practical LSTM implementation that predicts the next word based on previous context. Trained on variable-length word sequences with real-world text data.

**Dataset:** Kaggle Next Word Prediction Dataset  
**Vocabulary Size:** 8,646 unique words  
**Model Type:** Sequential LSTM  
**Model Size:** Lightweight & efficient  

---

## 🏗️ Model Architecture

```
INPUT (Variable length word sequences)
    ↓
LSTM Layer 1
├─ Units: 512
├─ Return sequences: True
└─ Processes entire sequence

LSTM Layer 2
├─ Units: 256
├─ Return sequences: False
└─ Outputs final state only

Dense Layer (Softmax)
├─ Units: 8,646 (vocabulary size)
├─ Activation: Softmax
└─ Probability distribution over all words

OUTPUT (Next word prediction)
```

### Model Summary

```
Total Parameters: ~2.5M
Trainable Parameters: 100%
Model Size: ~10 MB
```

---

## 📊 How It Works

1. **Data Loading** - Download from Kaggle Hub
2. **Text Processing** - Lowercase, remove special characters
3. **Tokenization** - Convert words to integers
4. **Sequence Creation** - Create variable-length sequences
5. **Model Training** - Train LSTM on sequence patterns
6. **Prediction** - Generate next word probabilities

---

## 🚀 Quick Start

### Requirements
```bash
pip install tensorflow keras numpy pandas kagglehub
```

### Setup
```python
import kagglehub

# Download dataset
path = kagglehub.dataset_download("ronikdedhia/next-word-prediction")
```

### Training
```bash
jupyter notebook LSTM-next-word-pred.ipynb
```

---

## 📈 Features

✅ **Variable Length Input** - Handles different context lengths  
✅ **Kaggle Dataset** - Real-world text data  
✅ **Efficient Model** - Only 2.5M parameters  
✅ **Fast Training** - Quick convergence  
✅ **Large Vocabulary** - 8,646 words  

---

## 💡 Use Cases

- Text autocomplete
- Search suggestions
- Email predictions
- Chat assistance
- Code completion

---

## 📝 Training Details

```
Optimizer: Adam
Loss: Categorical Crossentropy
Metrics: Accuracy
Batch Size: 32
Epochs: Variable
```

---

## 🔄 Prediction Pipeline

```
Input Text: "The quick brown"
    ↓
Tokenize: [word_id_1, word_id_2, word_id_3]
    ↓
LSTM Processing: Learn patterns
    ↓
Output: [0.01, 0.03, ..., 0.08, ...] (8646 values)
    ↓
argmax(): Get highest probability word
    ↓
Decode: "fox" (or other predicted word)
```

---

## 🎓 Key Concepts

**LSTM vs Traditional RNN:**
- LSTM handles long-term dependencies
- Prevents vanishing gradient problem
- Better for sequential text data

**Variable Length Sequences:**
- More flexible than fixed-length
- Better represents natural text
- Model learns at different context depths

---

## 📁 Files Generated

- `model.h5` - Trained model weights
- `tokenizer.pkl` - Word-to-integer mappings

---

## 🔧 Advanced Features

**Model Customization:**
- Adjust LSTM units (128, 256, 512, 1024)
- Add Dropout layers
- Implement bidirectional LSTM
- Use GRU instead of LSTM

**Data Enhancement:**
- Add more text sources
- Increase vocabulary size
- Balance sentence lengths

---

## 📊 Advantages of This Model

✅ **Lightweight** - Only 2.5M parameters  
✅ **Fast** - Quick training & inference  
✅ **Flexible** - Handles variable-length input  
✅ **Effective** - Good accuracy with less computation  
✅ **Practical** - Works for real-world applications  

---

## 🐛 Troubleshooting

**Issue: Kaggle dataset download fails**
- Solution: Create Kaggle API token, place in ~/.kaggle/

**Issue: Out of memory**
- Solution: Reduce batch size, reduce sequence length

**Issue: Poor accuracy**
- Solution: Increase epochs, add more data, tune hyperparameters

---

## 📚 Technologies Used

- **TensorFlow/Keras** - Deep learning
- **Tokenizer** - Text preprocessing
- **LSTM** - Sequential modeling
- **Kaggle Hub** - Data source

---

## 📝 Author

**Furqan** | AI Engineer & Lead AI Trainer  
Saylani Mass IT Training (SMIT)  
Karachi, Pakistan

Building practical AI solutions for real-world problems

---

## 📄 License

MIT License

---

**Ready to predict words faster than you can think!** 🚀
