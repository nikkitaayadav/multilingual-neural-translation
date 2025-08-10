# Multilingual Neural Translation (English–Hindi)

This project develops a neural machine translation system for English–Hindi and Hindi–English using transformer-based architectures mBART and mT5. The goal was to achieve high translation quality with strong semantic and contextual alignment, while also comparing the strengths and limitations of each model.

## Project Overview

- Used the **IIT Bombay English–Hindi Parallel Corpus** (1.49M+ parallel sentences) spanning diverse domains
- Applied **mBART** (pre-trained for translation) and **mT5** (general text-to-text framework) for supervised fine-tuning
- Conducted extensive preprocessing, tokenization, and special token handling for multilingual embeddings
- Tuned hyperparameters including learning rates, schedulers, batch sizes, BF16 precision, and frozen encoder layers (mT5)
- Evaluated using **BERTScore** for semantic similarity and contextual alignment
- I contributed primarily to **data preprocessing**, **training pipeline setup**, **experiment tracking**, and **evaluation analysis**

This was a collaborative academic project for the University of Houston’s **Natural Language Processing** course.

## Files Included

- `notebook.ipynb`: End-to-end training and evaluation code for mBART and mT5 models
- `report.pdf`: Detailed write-up including dataset details, preprocessing, methodology, results, and discussion
- `presentation.pptx`: Summary of approach, model architectures, results, and challenges

## Dataset Source

- IIT Bombay English–Hindi Parallel Corpus: [https://www.cfilt.iitb.ac.in/iitb_parallel/](https://www.cfilt.iitb.ac.in/iitb_parallel/)

## Key Results

| Model | Direction | Precision (%) | Recall (%) | F1 Score (%) |
|-------|-----------|---------------|------------|--------------|
| mBART | English→Hindi | 95.5 | 92.0 | 93.7 |
| mBART | Hindi→English | 98.4 | 98.9 | 98.7 |
| mT5   | English→Hindi | 77.3 | 77.5 | 77.2 |

**Observations:**
- mBART excelled in both translation directions, handling idiomatic and culturally specific phrases with high accuracy.
- mT5 performed adequately for simple sentences but struggled with complex structures and idiomatic expressions.
- Dataset quality and linguistic complexity posed challenges for both models.

## Acknowledgments

- Pre-trained checkpoints from [Hugging Face Transformers](https://huggingface.co/)
- mBART50Tokenizer and MT5Tokenizer for multilingual embeddings

## Notes

The repository contains source code, documentation, and presentation material to enable reproduction of the training and evaluation process. Large raw datasets are not included; please use the official dataset link to download the corpus.
