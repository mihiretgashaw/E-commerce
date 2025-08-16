# EthioMart Telegram E-commerce Data Extractor

## Project Overview
This project extracts and analyzes product data from Ethiopian Telegram channels to support micro-lending decisions for small vendors. 
It leverages Named Entity Recognition (NER) models to identify products and prices, evaluates model performance, explains predictions with interpretability tools, and calculates vendor metrics such as posting frequency, average views, and lending scores.

## Key Features
- **Telegram Data Scraper:** Collects posts and metadata (timestamps, views, prices) from vendor channels.
- **NER Modeling:** Fine-tunes DistilBERT, XLM-Roberta, and mBERT models to extract product and price entities.
- **Model Comparison:** Evaluates NER model performance across metrics like F1-score, precision, and recall.
- **Interpretability:** Uses SHAP and LIME to explain model predictions and ensure trustworthiness.
- **Vendor Analytics Engine:** Computes metrics for each vendor:
  - Posting frequency (posts/week)
  - Average views per post
  - Average product price
  - Top-performing posts
  - Lending score (custom weighted score combining engagement and activity)
- **Visualizations:** Generates bar charts and scatter plots for quick insights into vendor performance.

## Project Structure
E-commerce/
├── notebooks/ # Jupyter notebooks
│ ├── 04_model_comparison.ipynb # Compare NER models
│ ├── fine_tune.ipynb # Fine-tune NER models
│ ├── Interpretability.ipynb # SHAP / LIME explanations
│ ├── label.ipynb # Raw data labeling
│ ├── labeling.ipynb # Data labeling process
│ ├── preprocess.ipynb # Data cleaning and preparation
│ ├── score_card.ipynb # Generate vendor scorecards & visualizations
│ ├── DistilBERT_ner_model/ # DistilBERT checkpoints
│ ├── DistilBERT_ner_model_final/
│ ├── XLM-Roberta_ner_model/
│ ├── XLM-Roberta_ner_model_final/
│ ├── mBERT_ner_model/
│ ├── mBERT_ner_model_final/
│ └── models/ # Any additional models
├── data/ # Raw and processed datasets
├── vendor_scorecard.csv # Vendor metrics CSV
├── vendor_lending_score.png # Vendor score visualizations
└── README.md # Project documentation
