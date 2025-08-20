# LLM-Fine-Tuned DistilBERT Text Classification Model

## ModelThis project fine-tunes [`huawei-noah/TinyBERT_General_4L_312D`](https://huggingface.co/huawei-noah/TinyBERT_General_4L_312D) from Hugging Face Transformers on a binary classification task. It is a lightweight BERT model designed for speed and efficiency on resource-constrained environments.

It handles class imbalance through careful data splitting and evaluation.
**Why TinyBERT?**
- Much faster and smaller than BERT-base
- Suitable for deployment on low-resource devices
## Files
- `LLM.ipynb` — Jupyter notebook for data preprocessing, model training, and evaluation.
- `requirements.txt` — Python packages required to run this project.
- `finetuned_distilbert/` — Saved model directory (contains tokenizer and model files).
- `README.md` — Project documentation (this file).
## Setup
To install dependencies, run:
```bash
pip install -r requirements.txt
```
This project fine-tunes `distilbert-base-uncased` on a binary text classification dataset with class imbalance.

## Dependencies
- Python 3.8+ recommended
- See requirements.txt for required packages
  
## Evaluation
Includes precision, recall, and F1-score for unseen test data.
## Evaluation Results
The model was evaluated on an unseen test set with the following results:
| Class | Precision | Recall | F1-Score | Support |
| ----- | --------- | ------ | -------- | ------- |
| 0     | 0.9743    | 0.9773 | 0.9758   | 5633    |
| 1     | 0.8131    | 0.7934 | 0.8032   | 702     |
Accuracy: 0.9569 (total 6335 samples)
Note: Class 1 is underrepresented in the dataset, which may explain the lower F1-score.

## Usage
- Prepare your dataset in the same format (binary labels).
- Fine-tune the model using the training script (train.py if available).
- Evaluate on the test set using the evaluation script (eval.py if available).

## Notes
- This project demonstrates handling class imbalance in a binary classification task.
- Can be extended with class weighting, oversampling, or other techniques for improved performance on minority class.


