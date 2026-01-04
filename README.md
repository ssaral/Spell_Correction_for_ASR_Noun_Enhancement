# Spell Correction for ASR Noun Enhancement

## Project Overview
This repository contains an **end-to-end NLP project on spell correction for Automatic Speech Recognition (ASR) outputs**, with a **special focus on noun and medical terminology correction**.

ASR systems frequently introduce spelling, phonetic, and segmentation errors—particularly for **medication names and medical nouns**. This project investigates these challenges through detailed data analysis, multiple modeling approaches, and extensive evaluation.

The repository is **documentation- and experiment-driven**, containing:
- A comprehensive technical report (primary reference)
- Experimental outputs (CSV files)
- Visual analysis and evaluation plots
- A complete Jupyter notebook implementation

---

## Technical Reports

### Primary Technical Report
**`Technical_Report.pdf`**  
The main technical document covering:
- Dataset analysis and EDA
- Error extraction and classification
- Data preprocessing and splitting
- Model architectures and training
- Evaluation metrics and results
- Error analysis, challenges, and future work

### Assignment Submission Report
**`ASR-NLP_Assignment_Spell_Correction_for_ASR_Noun_Enhancement.pdf`**  
Formatted version of the technical report prepared specifically for assignment submission.

> **For complete methodology, results, and conclusions, refer to the PDF reports.**

---

## Repository Structure

```
.
├── ASR-NLP_Assignment_Spell_Correction_for_ASR_Noun_Enhancement.pdf
├── Technical_Report.pdf
│
├── spell_correction_asr_complete.ipynb   # End-to-end implementation notebook
│
├── csv                                  # Experimental outputs & datasets
│   ├── advanced_model_predictions.csv
│   ├── baseline_all_predictions.csv
│   ├── baseline_dictionary_predictions.csv
│   ├── baseline_edit_distance_predictions.csv
│   ├── baseline_ngram_predictions.csv
│   ├── error_database_full.csv
│   ├── error_general_nouns.csv
│   └── error_medications.csv
│
├── graphs                               # Plots & visualizations used in report
│   ├── 01_eda_analysis.png
│   ├── 04_model_metrics_comparison_full.png
│   ├── 07_error_type_heatmap.png
│   ├── 07_length_impact_analysis.png
│   ├── 07_noun_radar_chart.png
│   └── error_word_extraction.png
│
└── README.md
```

---

## Problem Statement
Automatic Speech Recognition systems perform poorly on:
- Medical terminology
- Medication names
- Phonetically complex nouns
- Hyphenated and segmented words

This project aims to:
- Analyze ASR spelling errors at scale
- Extract and categorize noun-specific errors
- Evaluate multiple correction strategies
- Quantify performance gaps between general and medical nouns

---

## Models Implemented

1. **Baseline Ensemble Model**
   - Edit distance–based correction
   - N-gram language model
   - Dictionary-based lookup

2. **Advanced Transformer Model (T5)**
   - Seq2Seq text-to-text correction
   - Best-performing model overall

3. **BERT Token Classification Model**
   - Error detection–oriented approach
   - Demonstrated architectural mismatch for correction

4. **Custom Noun-Specific Model**
   - Designed to prioritize noun correction
   - Limited by data imbalance and scale

---

## Evaluation Metrics
Models are evaluated using:
- Word-level Accuracy
- Character-level Accuracy
- BLEU Score
- Exact Match Accuracy
- Edit Distance Score
- **Noun-specific Accuracy (key focus)**

All evaluation results are available in:
- `csv/` (raw predictions and error databases)
- `graphs/` (visual summaries)

---

## Key Findings (High-Level)
- **Best Overall Model:** T5 Transformer
- **Best Word-level Accuracy:** ~79%
- **Medical Noun Accuracy:** ~48% (primary limitation)
- **Baseline models** performed surprisingly well given their simplicity
- **Medical noun correction remains the hardest problem** due to class imbalance and data scarcity

---

## Challenges Identified
- Severe imbalance between general nouns and medical nouns (≈12:1)
- Poor segmentation handling for medication names
- Limited generalization to rare or unseen drugs
- Architectural mismatch in token-classification approaches

---

## Future Work
Recommended improvements include:
- Incorporating larger medical corpora
- Using domain-specific models (BioBERT, SciBERT)
- Adding medication dictionary–constrained decoding
- Explicit segmentation modeling (CRF, morphological rules)

---

## How to Explore This Project
1. **Read the technical report** (`Technical_Report.pdf`) for full context
2. **Open the notebook** (`spell_correction_asr_complete.ipynb`) to review implementation
3. **Inspect CSV files** for predictions and error analysis
4. **View graphs/** for visual insights used in the report

---

## Author
**Saral Sureka**  
NLP Assignment – Spell Correction for ASR (Self-assigned)
November 28, 2025

---

## Notes
- This repository prioritizes **analysis, evaluation, and documentation**
- The PDFs are the authoritative source for all technical decisions
- Code is provided in notebook form for clarity and reproducibility

---

If you intend to extend this work (research, production, or coursework), start with the technical report and error analysis sections.

