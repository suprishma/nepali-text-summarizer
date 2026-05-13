# Nepali Text Summarizer

Abstractive text summarization for the Nepali language using fine-tuned mBART transformer model.

## Overview
Fine-tuned `facebook/mbart-large-50` on a custom Nepali news dataset using 
LoRA (Low-Rank Adaptation) for efficient training.

## Model Details
- Base model: `facebook/mbart-large-50`
- Fine-tuning method: LoRA (r=16, alpha=32)
- Language: Nepali (`ne_NP`)
- Task: Abstractive Summarization

## Results
| Epoch | Training Loss | Validation Loss |
|-------|--------------|-----------------|
| 1     | 1.5116       | 1.7374          |
| 2     | 1.4108       | 1.3529          |
| 3     | 1.3360       | 1.3398          |

## Tech Stack
- Python, HuggingFace Transformers
- PEFT (LoRA), mBART
- Google Colab (GPU)

## Dataset
Nepali news articles with summaries, sourced from Kaggle.  
Dataset: (https://www.kaggle.com/datasets/adarsh203/nepali-news-article-with-summary))
