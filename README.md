# DSA4213 Assignment 3 — Sentiment Classification & Analysis

This project implements sentiment classification on the IMDb dataset using BERT and DistilBERT, under three fine-tuning strategies: Full Fine-tuning, LoRA, and Prompt Tuning.  
It includes data cleaning, exploratory analysis, model training, evaluation, qualitative error analysis, and toxicity analysis.

All results and generated files are included in this repository.

---

## Contents

- **Data Cleaning:** Removes duplicates and splits IMDb data into train/test sets with zero overlap.  
- **EDA:** Visualizes label distribution and review lengths.  
- **Model Training:** Fine-tunes BERT and DistilBERT using full, LoRA, and prompt tuning approaches.  
- **Evaluation:** Computes accuracy, precision, recall, F1, and confusion matrices for all models.  
- **Qualitative Analysis:** Extracts and saves misclassified examples for error inspection.  
- **Toxicity Analysis:** Uses `unitary/toxic-bert` to score toxicity of reviews and summarizes results.

---
## Usage

1. **Install requirements**

   ```bash
   pip install -r requirements.txt

2. **Run the notebook**
Open DSA 4213 assignment 3.ipynb in VS Code and execute cells sequentially.

3. **Outputs**
**Quantitative Evaluation**
- model_evaluation_summary.csv -Contains accuracy, precision, recall, and F1 scores for each model.
- prompt_tuning_results.csv -Summary of prompt tuning results for BERT and DistilBERT.

**Predictions**
- bert_full_finetuned_predictions.csv - Predictions from BERT full fine-tuned model.
- distilbert_full_finetuned_predictions.csv - Predictions from DistilBERT full fine-tuned model.
- bert_lora_finetuned_predictions.csv - Predictions from BERT LoRA fine-tuned model.
- distilbert_lora_finetuned_predictions.csv - Predictions from DistilBERT LoRA fine-tuned model.
- bert_prompt_finetuned_predictions.csv - Predictions from BERT prompt-tuned model.
- distilbert_prompt_finetuned_predictions.csv - Predictions from DistilBERT prompt-tuned model.

**Qualitative error analysis**
- *_qualitative_errors.csv
  (e.g. bert_full_finetuned_qualitative_errors.csv)
  Contains misclassified examples for each model, useful for error inspection.

**Toxicity Analysis**
- *_with_toxicity.csv
  (e.g. bert_full_finetuned_predictions_with_toxicity.csv)
  Adds toxicity scores to each prediction.
- toxicity_comparison_summary.csv
  Summarizes average toxicity scores across all models.
---
4. **Notes**
Models are saved in folders like bert_full_finetuned, distilbert_lora_finetuned, etc.
Cleaned dataset is saved at ./clean_imdb_dataset.
All CSVs are generated automatically when running the notebook.

---
5. **Requirements**
See requirements.txt for dependencies.
