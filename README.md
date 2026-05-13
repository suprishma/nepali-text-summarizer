# Nepali Text Summarizer

Automatic summarization of Nepali news articles using NLP techniques.
Nepali is a low-resource language with limited NLP support, making summarization
a challenging task. This project explores both extractive and abstractive approaches
to find the most effective solution.

## Approaches

**Extractive:** Sentences are scored and selected from the original text using a
combination of TF-IDF, TextRank (graph-based PageRank), and semantic sentence
embeddings. Final score is a weighted combination of all three methods.

**Abstractive:** Transformer models are fine-tuned to generate new human-like
summaries. Experimented with mT5-small (with and without LoRA) before settling
on mBART-large-50 with LoRA as the final model. mBART was chosen due to its
multilingual pretraining on 50 languages including Nepali (`ne_NP`), giving it
a stronger foundation for low-resource summarization.

## Results (mBART)

| Metric  | Precision | Recall | F1    |
|---------|-----------|--------|-------|
| ROUGE-1 | 0.507     | 0.571  | 0.537 |
| ROUGE-2 | 0.278     | 0.324  | 0.299 |
| ROUGE-L | 0.451     | 0.508  | 0.478 |

## Tech Stack
Python, HuggingFace Transformers, PEFT (LoRA), sentence-transformers, Google Colab

## Dataset
[Nepali News Article with Summary](https://www.kaggle.com/datasets/adarsh203/nepali-news-article-with-summary)
