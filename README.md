# Enhancing Sentiment Classification on Small Datasets through Data Augmentation and Transfer Learning

This repository contains code and experiments supporting the study **"Enhancing Sentiment Classification on Small Datasets through Data Augmentation and Transfer Learning"** by Mahmoud Mayaleh and Samer Mayaleh.

## Overview

The project investigates the impact of various data augmentation techniques on sentiment classification performance when training data is limited. It compares:

- Easy Data Augmentation (EDA)  
- NLPaug (contextual augmentation)  
- Back-Translation  

Classical machine learning models (Logistic Regression, Random Forest) and a fine-tuned BERT model are evaluated on original and augmented datasets.

## Key Features

- Data augmentation methods for text classification  
- Training and evaluation of classical ML models with cross-validation  
- Transfer learning with BERT for sentiment classification  
- Performance metrics: Accuracy, F1-score, AUC  
- Confidence interval calculations for robustness analysis  

## Getting Started

### Requirements

- Python 3.7+  
- Libraries: `scikit-learn`, `pandas`, `transformers`, `torch`, `nlpaug`, `googletrans`, `datasets`  

## Usage

- Prepare dataset (IMDB small subset used here)  
- Apply augmentation techniques  
- Train and evaluate classical ML models  
- Fine-tune BERT model with transfer learning  
- Generate performance reports with confidence intervals  

## Results

The experiments show that data augmentation improves classification performance on small datasets. Among traditional models, Random Forest combined with NLPaug augmentation achieved notable gains, with accuracy reaching up to 96.9%. Logistic Regression also benefited from augmentation, especially with NLPaug and EDA.

For the BERT model, fine-tuning on the original dataset led to gradual performance improvements over training epochs, reaching about 88% accuracy at epoch 70. However, fine-tuning BERT on the combined Original + NLPaug augmented dataset resulted in a substantial boost, with accuracy consistently above 99.5% across different random seeds (12, 44, 127). This highlights the effectiveness of contextual augmentation and transfer learning in low-resource sentiment classification.

Overall, BERT with augmentation outperformed traditional models by a wide margin, demonstrating the value of enriched training data and transformer-based models in sentiment analysis tasks.

| Model           | Dataset              | Accuracy | F1-Score | AUC    |
|-----------------|----------------------|----------|----------|--------|
| Random Forest   | Original             | 84.6%    | 84.3%    | 92.4%  |
| Random Forest   | Original + NLPaug    | 96.9%    | 96.8%    | 99.7%  |
| BERT            | Original             | 88.0%    | 87.0%    | 87.7%  |
| BERT            | Original + NLPaug    | 99.5%    | 99.5%    | 99.8%  |

## Citation

If you use this work, please cite:

Mahmoud Mayaleh and Samer Mayaleh,  
*"Enhancing Sentiment Classification on Small Datasets through Data Augmentation and Transfer Learning: A Comparative Study,"* May 2025.

## License
MIT License
