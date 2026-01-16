# multilingual-emotion-detection-baseline-vs-hpo
## Overview
This repository presents a multilingual emotion classification project focusing on the comparison between a reproducible baseline and Hyperparameter Optimization (HPO) using Transformer-based models.

The primary goal is not only to improve final scores, but to analyze how hyperparameter changes affect model behavior, error patterns, and cross-lingual generalization.

The project includes:
- A clearly defined baseline
- Systematic HPO experiments
- Quantitative evaluation (Macro-F1, Accuracy, Confusion Matrix)
- Qualitative and deep error analysis
- Full reproducibility details


## Models
- Transformer-based multilingual models (e.g. XLM-RoBERTa)
- Fine-tuned for emotion classification
- Evaluated on both English and Turkish datasets. GoEmotion Dataset as English and Turkish Tweets Dataset as Turkish datasets:
- https://www.kaggle.com/datasets/anil1055/turkish-tweet-dataset/data
- https://www.kaggle.com/datasets/debarshichanda/goemotions

## Experiments
### Baseline

- Fixed architecture
- Fixed training configuration
- Serves as a fair and reproducible reference point

### Hyperparameter Optimization (HPO)

- Learning rate variations
- Epoch number adjustments
- Comparative analysis across languages
- Focus on behavioral changes, not only final metrics

## Evaluation Metrics
- Accuracy
- Macro-F1 Score
- Confusion Matrix
- Manual error categorization

## Deep Error Analysis
Errors are manually categorized into:

- Confusion between close emotions
- Ambiguous or context-dependent expressions
- Dataset labeling inconsistencies
- Cross-lingual semantic mismatch

This analysis reveals that some model “errors” stem from annotation noise rather than model failure.


## Reproducibility Notes
To ensure reproducibility:

- All random seeds are fixed
- Baseline hyperparameters are explicitly defined
- HPO search space is documented
- Training and evaluation are performed using the same data splits
- Experiments were conducted using the same evaluation pipeline


## Environment
- Kernel was chosen as Python 3.11.0
- HuggingFace Transformers
- Scikit-learn
- accelerate>=0.26.0

