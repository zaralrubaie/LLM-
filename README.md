# LLM-Fine-Tuned DistilBERT Text Classification Model

##ModelThis project fine-tunes [`huawei-noah/TinyBERT_General_4L_312D`](https://huggingface.co/huawei-noah/TinyBERT_General_4L_312D) from Hugging Face Transformers on a binary classification task. It is a lightweight BERT model designed for speed and efficiency on resource-constrained environments.

It handles class imbalance through careful data splitting and evaluation.
**Why TinyBERT?**
- Much faster and smaller than BERT-base
- Suitable for deployment on low-resource devices
## Files
- `LLM.ipynb` — Jupyter notebook for data preprocessing, model training, and evaluation.
- `requirements.txt` — Python packages required to run this project.
- `finetuned_distilbert/` — Saved model directory (contains tokenizer and model files).
- `README.md` — Project documentation (this file).
##Setup
To install dependencies, run:
```bash
pip install -r requirements.txt
This project fine-tunes `distilbert-base-uncased` on a binary text classification dataset with class imbalance.
## Dependencies
See `requirements.txt` to install required packages.

## Evaluation
Includes precision, recall, and F1-score for unseen test data.

##Evaluation Results
The model was evaluated on an unseen test set with the following results:
          precision    recall  f1-score   support

       0     0.9743    0.9773    0.9758      5633
       1     0.8131    0.7934    0.8032       702

accuracy                         0.9569      6335
[macro avg 0.8937 0.8854 0.8895 6335]
[weighted avg 0.9565 0.9569 0.9567 6335]
These metrics demonstrate strong generalization, especially in class-imbalanced scenarios.


