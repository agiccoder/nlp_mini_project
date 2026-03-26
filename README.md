# Consumer Complaint Classification under Small-Data Constraints

Mini-project for **Natural Language Processing (NLP) in Python**.

## Final submission contents

```text
NLP_project_updated/
├── README.md
├── consumer_complaints.ipynb
├── consumer_complaints_small.csv
├── requirements.txt
├── artifacts/
│   ├── single_run_results.csv
│   ├── subsample_study_runs.csv
│   ├── subsample_study_summary.csv
│   ├── macro_f1_mean_table.csv
│   ├── macro_f1_std_table.csv
│   ├── accuracy_mean_table.csv
│   ├── model_comparison_compact.png
│   ├── macro_f1_vs_size.png
│   ├── accuracy_vs_size.png
│   ├── confusion_matrix_tfidf_seed42.png
│   ├── top_confusions_tfidf_seed42.csv
│   └── error_analysis_examples.csv
├── report/
│   ├── consumer_complaint_report.tex
│   └── consumer_complaint_report.pdf
└── presentation/
    ├── consumer_complaint_presentation.tex
    └── consumer_complaint_presentation.pdf
```

## Main notebook

Use this notebook for grading and reproduction:

- **`consumer_complaints.ipynb`**

## Main finding

**TF-IDF + Logistic Regression performs best across all dataset sizes.**  
Local Word2Vec improves as more in-domain data becomes available and consistently outperforms Pretrained GloVe, but neither embedding-based model surpasses the classical baseline.

## Error analysis added

This updated repo now includes:

- `artifacts/confusion_matrix_tfidf_seed42.png`
- `artifacts/top_confusions_tfidf_seed42.csv`
- `artifacts/error_analysis_examples.csv`

The main recurring mistakes are:

- **Debt collection ↔ Credit reporting**
- **Bank account or service ↔ Credit card**
- occasional **Mortgage ↔ Bank account or service** overlap

## How to run

Install dependencies:

```bash
pip install -r requirements.txt
```

Open and run:

```bash
jupyter notebook consumer_complaints.ipynb
```

Make sure `consumer_complaints_small.csv` is in the project root.

### Optional GloVe run
For the pretrained GloVe section, place:

- `glove.6B.100d.txt`

in the project root, or update the path in the notebook accordingly.

## Report and presentation

- Report source: `report/consumer_complaint_report.tex`
- Report PDF: `report/consumer_complaint_report.pdf`
- Presentation source: `presentation/consumer_complaint_presentation.tex`
- Presentation PDF: `presentation/consumer_complaint_presentation.pdf`
