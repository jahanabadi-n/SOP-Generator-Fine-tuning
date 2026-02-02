# SOP Generator - Fine-tuning LLM for Graduate School Applications

Fine-tuning a Large Language Model (Llama 3.1 8B) to generate high-quality Statements of Purpose for graduate school applications.

## 📋 Project Overview

This project implements an end-to-end pipeline for:
- Collecting and augmenting Statement of Purpose (SOP) datasets
- Fine-tuning open-source LLMs using QLoRA
- Deploying a web interface for SOP generation

## 🎯 Motivation

Graduate school applications require compelling SOPs, but many applicants struggle with writing them. This project aims to democratize access to quality SOP writing assistance through fine-tuned AI.

## 📊 Dataset

- **Size:** 500+ SOPs across multiple disciplines
- **Sources:** 
  - 60 real-world SOPs (collected from public sources)
  - 300 augmented variations (paraphrasing, tone shifts)
  - 140 synthetic SOPs (generated via GPT-4o)
- **Focus:** Computer Science and related fields

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

## 🚀 Getting Started

Coming soon...

## 📈 Results

Coming soon...

## 🤝 Contributing

This is a personal project for learning purposes.

## 📝 License

MIT License

## 👤 Author

[Your Name]
- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)

---

**Status:** 🚧 Work in Progress
