# SOP Generator — LLM Fine-tuning for Graduate Applications

A learning-focused AI project for preparing a Statement of Purpose (SOP) dataset and fine-tuning an instruction-following language model to generate graduate school SOP drafts.

The current repository focuses on the data preparation stage and documents the planned fine-tuning workflow.

---

## 📋 Project Overview

This project is designed as an end-to-end SOP generation pipeline:

- Collect and organize Statement of Purpose examples
- Augment and format SOP data for instruction fine-tuning
- Split the dataset into training and validation sets
- Fine-tune an open-source language model using LoRA / QLoRA
- Evaluate generated SOP quality
- Build a simple inference interface for generation

---

## 🎯 Motivation

Graduate school applicants often struggle to structure strong Statements of Purpose. This project explores how fine-tuned language models can assist with generating structured SOP drafts while preserving a clear, domain-specific writing style.

This is a learning project focused on practical LLM fine-tuning, dataset preparation, and model evaluation.

---

## 🛠️ Technical Stack

- Python
- Jupyter Notebook / Google Colab
- Hugging Face Transformers
- Datasets
- PyTorch
- PEFT / LoRA
- Gradio planned for demo deployment

---

## 📁 Repository Structure

```text
SOP-Generator-Fine-tuning/
│
├── notebooks/
│   └── 01_data_preparation.ipynb   # Dataset loading, formatting, splitting, and export
│
├── requirements.txt                # Python dependencies
└── README.md
```

---

## ✅ Current Status

**Status:** Work in Progress

Completed:

- Built a data preparation notebook
- Loaded SOP files from multiple sources
- Parsed SOP text and field metadata
- Converted samples into instruction-tuning chat format
- Split the dataset into training and validation sets
- Exported prepared data to JSONL format

Planned:

- Add model fine-tuning notebook
- Add evaluation notebook
- Add inference notebook
- Add Gradio demo
- Add sample generated SOP outputs

---

## 📊 Dataset Preparation

The data preparation notebook processes a dataset of 500 SOP examples:

- **60** original SOP samples
- **300** augmented SOP samples
- **140** synthetic SOP samples
- **500** total examples

The dataset is converted into chat-style instruction fine-tuning format:

```json
{
  "messages": [
    {"role": "system", "content": "You are an expert at writing compelling Statements of Purpose for graduate school applications."},
    {"role": "user", "content": "Write a Statement of Purpose for a Master's program in Computer Science."},
    {"role": "assistant", "content": "...SOP text..."}
  ]
}
```

Split:

- **400** training examples
- **100** validation examples

---

## 📓 Notebooks

| Notebook | Description | Status |
|---|---|---|
| [`01_data_preparation.ipynb`](notebooks/01_data_preparation.ipynb) | Loads SOP data, parses metadata, formats examples, splits dataset, and exports JSONL files | Completed |
| `02_model_training.ipynb` | Fine-tuning pipeline using LoRA / QLoRA | Planned |
| `03_evaluation.ipynb` | Evaluation of generated SOP quality | Planned |
| `04_inference.ipynb` | Inference and demo testing | Planned |

---

## 🚀 Planned Training Setup

Target setup:

- Open-source instruction model such as Llama 3.x Instruct
- LoRA or QLoRA parameter-efficient fine-tuning
- Hugging Face `Trainer` / `SFTTrainer`
- Kaggle or Colab GPU environment
- Evaluation using validation loss and qualitative SOP samples

---

## ⚠️ Known Limitations

- Dataset quality depends on original, augmented, and synthetic SOP quality
- Some samples may contain generic or template-like language
- No deployed inference demo yet
- Model fine-tuning notebook is not yet included in the repository
- Generated SOPs should be treated as drafts, not final application essays

---

## 🔮 Future Improvements

- Add fine-tuning notebook and training logs
- Add sample generated SOPs before and after fine-tuning
- Add evaluation metrics such as ROUGE or BERTScore
- Add Gradio demo for interactive SOP generation
- Improve dataset cleaning and remove low-quality templates
- Add prompt templates for different graduate fields

---

## 👤 Author

**Ali Alavi**  
AI/ML Enthusiast

- GitHub: [salavii](https://github.com/salavii)
- LinkedIn: [linkedin.com/in/ali-alavi-cs](https://linkedin.com/in/ali-alavi-cs)
