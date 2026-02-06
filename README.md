# SOP Generator - Fine-tuning LLM for Graduate School Applications

Fine-tuning a Large Language Model (Llama 3.1 8B) to generate high-quality Statements of Purpose for graduate school applications.

## 📋 Project Overview

This project implements an end-to-end pipeline for:
- Collecting and augmenting Statement of Purpose (SOP) datasets
- Fine-tuning open-source LLMs using QLoRA
- Deploying a web interface for SOP generation

## 🎯 Motivation

Graduate school applications require compelling SOPs, but many applicants struggle with writing them. This project aims to democratize access to quality SOP writing assistance through fine-tuned AI.

## 🛠️ Technical Stack

- **Model:** Llama 3.1 8B
- **Fine-tuning:** QLoRA (4-bit quantization)
- **Framework:** PyTorch, Transformers, PEFT
- **Deployment:** Gradio + HuggingFace Spaces

## 📁 Repository Structure
```
├── notebooks/
│   ├── 01_data_preparation.ipynb    # Data collection & preprocessing
│   ├── 02_model_training.ipynb      # Fine-tuning pipeline
│   ├── 03_evaluation.ipynb          # Model evaluation
│   └── 04_inference.ipynb           # Inference & testing
├── src/                              # Source code (if needed)
├── data/                             # Dataset (gitignored)
├── requirements.txt                  # Dependencies
└── README.md
```
## ✅ Project Status

**Completed!** Model successfully fine-tuned on Kaggle.

### Training Results

- **Model:** Llama 3.2 1B Instruct (1.23B parameters)
- **Method:** LoRA (Low-Rank Adaptation)
- **Trainable Parameters:** 0.2% (~2.8M / 1.23B)
- **Training Loss:** 2.18 → 1.86
- **Validation Loss:** 2.33 → 2.08
- **Training Time:** ~12 minutes (5 epochs)
- **Hardware:** Kaggle T4 GPU (15GB VRAM)
- **Dataset:** 400 training + 100 validation SOPs

### Dataset Composition

- **Original SOPs:** 60 real samples
- **Augmented SOPs:** 300 (via GPT-4o paraphrasing)
- **Synthetic SOPs:** 140 (GPT-4o generated)
- **Total:** 500 SOPs across 10 CS fields

### Notebooks

1. ✅ `01_data_preparation.ipynb` - Data collection, augmentation, and formatting
2. ✅ `02_model_training.ipynb` - Fine-tuning with LoRA on Kaggle

### Key Hyperparameters

- Learning Rate: 3e-4
- Batch Size: 2 (effective: 8 with gradient accumulation)
- Epochs: 5
- LoRA rank (r): 16
- Max sequence length: 1024 tokens

### Next Steps

- [ ] Create evaluation notebook (`03_evaluation.ipynb`)
- [ ] Deploy Gradio demo to HuggingFace Spaces
- [ ] Generate sample SOPs for portfolio

## 🚀 Getting Started

Coming soon...

## 📈 Results

Coming soon...

## 🤝 Contributing

This is a personal project for learning purposes.

## 📝 License

MIT License

## 👤 Author

Ali Alavi
- LinkedIn: [Your Profile](https://linkedin.com/in/ali-alavi-cs)

---

**Status:** 🚧 Work in Progress
