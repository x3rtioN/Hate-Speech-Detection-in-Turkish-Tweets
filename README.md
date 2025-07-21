# 🧠 Hate Speech Detection in Turkish Tweets (RNN + Attention)

This project aims to detect **hate speech** in Turkish tweets using deep learning models such as LSTM, BiLSTM, and GRU combined with different attention mechanisms. It includes preprocessing, Word2Vec embedding, model training, evaluation, and performance visualization.

---

## 📁 Contents

- `Untitled1.ipynb` — Main Jupyter Notebook with full implementation  
- `model_comparison_results.csv` — Final model evaluation results (Accuracy, F1, Precision, Recall)  
- `model_performance_comparison.png`, `confusion_matrix_*.png`, `training_metrics_*.png` — Visualizations of model performance

---

## 📌 Project Summary

- **Dataset:** Turkish tweets loaded from an Excel file  
- **Goal:** Binary classification – detect hate speech (label `1`) vs. normal content (`0`)  
- **Preprocessing (You can use Zemberek or something that performs exactly the same):**  
  - URL/HTML/character cleaning  
  - Text tokenization and sequence padding  
- **Embedding:**  
  - Turkish Word2Vec embedding (loaded or trained)  
  - Embedding matrix construction  
- **Models:**  
  - Three different RNN types: `LSTM`, `BiLSTM`, `GRU` combined with three different attention types: `Bahdanau`, `Luong`, `Scaled Dot-Product`
  - 9 different models compared with each other  
  - Word embeddings: pretrained or random  
- **Evaluation:**  
  - Accuracy, Precision, Recall, F1  
  - Confusion matrix visualization  
  - All results stored in CSV and plotted

---

## 📦 Requirements

```bash
pip install pandas numpy matplotlib seaborn tensorflow gensim scikit-learn openpyxl
```

You also need a Turkish Word2Vec model file named trword2vec_finetuned_local.model, or let the notebook train a new one.

## ▶️ How to Run

- Open Untitled1.ipynb in Jupyter Notebook
- Place the Excel file containing tweets in the same folder
- Run all cells — models will train and compare automatically
- Results will be saved as plots and CSV

## 📄 Visual Outputs

- Confusion matrices for each model
- Training loss and accuracy plots
- Heatmap comparing all models by the metrics

## 🧠 Customization Ideas

- You can modify: RNN types, attention types, epochs (kept it low because of the test cases), batch size, preprocessing pipeline
- Extend to multi-class classification if needed
