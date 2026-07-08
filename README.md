<div align="center">

# 📈 FinBERT-Finetuned
### Full-Parameter Fine-Tuning of FinBERT for Financial News Sentiment Analysis

<p align="center">

<img src="https://img.shields.io/badge/Python-3.12-blue?logo=python">
<img src="https://img.shields.io/badge/PyTorch-2.x-red?logo=pytorch">
<img src="https://img.shields.io/badge/HuggingFace-Transformers-yellow?logo=huggingface">
<img src="https://img.shields.io/badge/Transformers-4.x-orange">
<img src="https://img.shields.io/badge/Quantization-Dynamic-success">
<img src="https://img.shields.io/badge/NLP-FinBERT-blueviolet">
<img src="https://img.shields.io/badge/HuggingFace-Hub-gold?logo=huggingface">

</p>

**A production-ready Financial Sentiment Classification model obtained through full-parameter fine-tuning of FinBERT, optimized for financial news understanding, quantized for efficient inference, and deployed on Hugging Face Hub.**

</div>

---

# 🚀 Overview

This project improves the pretrained **FinBERT** model through **full-parameter supervised fine-tuning** on a curated financial news corpus.

Unlike lightweight adapter methods such as LoRA or prompt tuning, **all transformer parameters were updated**, enabling the model to better capture nuanced financial language while preserving generalization.

The final model was:

- ✅ Fully fine-tuned
- ✅ Dynamically quantized (INT8)
- ✅ Optimized for CPU inference
- ✅ Published to Hugging Face Hub

---

# ✨ Features

- 📈 Full-parameter fine-tuning of FinBERT
- 📰 Financial News Sentiment Classification
- ⚡ Dynamic INT8 Quantization
- 🤗 Hugging Face compatible model
- 💻 CPU-optimized inference
- 📊 Confidence score prediction
- 🚀 Production deployment ready

---

# 📊 Performance Improvements

| Metric | Baseline FinBERT | Fine-Tuned Model |
|---------|-----------------:|-----------------:|
| Validation Loss | **0.62** | **0.52** |
| Improvement | — | **≈16% reduction** |

### Highlights

- **≈16% lower validation loss**
- Better adaptation to mutual fund and stock-market news
- Improved prediction confidence on finance-specific vocabulary

---

# 🧠 Model Pipeline

```text
Financial Headlines
          │
          ▼
Text Cleaning
          │
          ▼
Tokenization
(Hugging Face Tokenizer)
          │
          ▼
Full Parameter Fine-Tuning
(FinBERT)
          │
          ▼
Validation
          │
          ▼
Dynamic Quantization
(INT8)
          │
          ▼
Hugging Face Hub
          │
          ▼
Inference API / Local Deployment
```

---

# 🏗️ Training Pipeline

```
Dataset Collection
        │
        ▼
Data Cleaning
        │
        ▼
Tokenization
        │
        ▼
Train / Validation Split
        │
        ▼
Full Parameter Fine-Tuning
        │
        ▼
Evaluation
        │
        ▼
Best Checkpoint Selection
        │
        ▼
Dynamic Quantization
        │
        ▼
Model Publishing
```

---

# 📚 Dataset

The model was trained on a curated financial sentiment dataset containing:

- Financial news headlines
- Market announcements
- Company-related news
- Mutual fund news
- Sector-specific financial events

### Label Distribution

- 🟢 Positive
- ⚪ Neutral
- 🔴 Negative

---

# 🧹 Data Preprocessing

The following preprocessing pipeline was used before training:

- HTML removal
- Lowercasing
- Whitespace normalization
- Financial text cleaning
- Tokenization using Hugging Face tokenizer
- Sequence padding
- Sequence truncation
- Attention mask generation

---

# ⚙️ Training Configuration

| Parameter | Value |
|-----------|------:|
| Model | FinBERT |
| Training Strategy | Full Parameter Fine-Tuning |
| Framework | Hugging Face Trainer |
| Optimizer | AdamW |
| Loss | Cross Entropy |
| Batch Training | Yes |
| Validation | Every Epoch |
| Device | GPU / CPU Compatible |

---

# ⚡ Quantization

After fine-tuning, the model was optimized using **PyTorch Dynamic Quantization**.

Benefits include:

- Reduced model size
- Faster CPU inference
- Lower memory usage
- Production-ready deployment

---

# 🤗 Hugging Face Hub

The final fine-tuned model is hosted on Hugging Face Hub.

```
https://huggingface.co/adillm/finsentim
```

The repository includes:

- config.json
- tokenizer.json
- tokenizer_config.json
- quantized_finbert_weights.pth

---

# 📂 Project Structure

```text
FinBERT-Finetuned
│
├── dataset/
│
├── notebooks/
│
├── training/
│
├── utils/
│
├── checkpoints/
│
├── quantized_model/
│   ├── config.json
│   ├── tokenizer.json
│   ├── tokenizer_config.json
│   └── quantized_finbert_weights.pth
│
├── inference.py
├── train.py
├── quantize.py
├── requirements.txt
└── README.md
```

---

# 🛠 Tech Stack

| Category | Technologies |
|----------|--------------|
| Language | Python |
| Deep Learning | PyTorch |
| NLP | Hugging Face Transformers |
| Tokenization | AutoTokenizer |
| Model | FinBERT |
| Optimization | Dynamic Quantization |
| Deployment | Hugging Face Hub |

---

# 📦 Major Libraries

```text
torch
transformers
datasets
accelerate
tokenizers
huggingface_hub
numpy
pandas
scikit-learn
```

---

# 🚀 Inference Example

```python
from transformers import AutoTokenizer
from transformers import AutoModelForSequenceClassification

tokenizer = AutoTokenizer.from_pretrained("adillm/finsentim")

model = AutoModelForSequenceClassification.from_pretrained(
    "adillm/finsentim"
)
```

---

# 📈 Applications

- Financial News Classification
- Stock Market Analytics
- Trading Systems
- Mutual Fund Analysis
- Portfolio Intelligence
- Financial Research
- Market Monitoring
- FinTech Applications

---

# 💡 Key Contributions

- Fine-tuned **all transformer layers** instead of using parameter-efficient adapters.
- Reduced validation loss by **≈16%** over the pretrained FinBERT baseline.
- Applied **dynamic INT8 quantization** for efficient CPU inference.
- Packaged the model in a reusable Hugging Face format for straightforward deployment.

<div align="center">

### ⭐ If you found this project useful, consider giving it a star!

</div>
