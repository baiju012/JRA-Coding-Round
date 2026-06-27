# English–Hindi Dataset Processing and Translation Assessment

## Overview

This repository contains the implementation and outputs for:

* **Assignment 1:** English–Hindi Dataset Processing and Analysis
* **Assignment 2:** English-to-Hindi Translation using a Large Language Model (LLM)

All tasks were completed using **Google Colab** and Python.

---

## Repository Structure

```text
English-Hindi-Assessment/
│
├── README.md
├── assignment1_and_2.ipynb
├── assignment1_cleaned_dataset.xlsx
├── assignment2_translation.xlsx
└── evaluation_scores.txt
```

---

## Assignment 1: English–Hindi Dataset Processing and Analysis

### Objective

The objective of this assignment was to process an English–Hindi parallel dataset and prepare a cleaned dataset according to the following requirements:

* Use at least 10,000 English–Hindi sentence pairs.
* Compute word counts for both English and Hindi sentences.
* Retain only those sentence pairs where both sentences contain 5 to 50 words.
* Calculate the difference between English and Hindi word counts.
* Keep only sentence pairs where the word count difference is between -10 and +10.
* Export the cleaned dataset to an Excel file.

### Output File

```text
assignment1_cleaned_dataset.xlsx
```

### Columns in the Excel File

1. English Sentences
2. Hindi Sentences
3. Word Count (English)
4. Word Count (Hindi)
5. Difference between Word Count (English) and Word Count (Hindi)

---

## Assignment 2: Translation with LLM

### Objective

The objective of this assignment was to:

* Select 100 English sentences from the cleaned dataset.
* Translate them into Hindi using a Large Language Model (LLM).
* Calculate BLEU, CHRF, and TER evaluation metrics.
* Save the translated sentences and evaluation scores.

### Translation Model Used

```text
Helsinki-NLP/opus-mt-en-hi
```

### Output Files

```text
assignment2_translation.xlsx
evaluation_scores.txt
```

### Columns in the Translation Excel File

1. Original English Sentence
2. Model-generated Hindi Translation

---

## Requirements

The following libraries were used in Google Colab:

```python
!pip install pandas openpyxl transformers sentencepiece sacrebleu datasets
```

---

## How to Run the Notebook in Google Colab

### Step 1: Open the Notebook

Open the file:

```text
assignment1_and_2.ipynb
```

in Google Colab.

### Step 2: Install Dependencies

Run the following command:

```python
!pip install pandas openpyxl transformers sentencepiece sacrebleu datasets
```

### Step 3: Clone the Dataset Repository

```bash
!git lfs install
!git clone https://huggingface.co/datasets/ainlpml/english-hindi
```

### Step 4: Run Assignment 1 Cells

The notebook will:

* Load the English and Hindi text files.
* Create a DataFrame with sentence pairs.
* Calculate English and Hindi word counts.
* Filter the dataset according to the assignment conditions.
* Generate:

```text
assignment1_cleaned_dataset.xlsx
```

### Step 5: Run Assignment 2 Cells

The notebook will:

* Select 100 English sentences from the cleaned dataset.
* Translate them into Hindi using the LLM.
* Calculate BLEU, CHRF, and TER scores.
* Generate:

```text
assignment2_translation.xlsx
evaluation_scores.txt
```

---

## Evaluation Metrics Used

The following evaluation metrics were used to evaluate translation quality:

* BLEU (Bilingual Evaluation Understudy)
* CHRF (Character n-gram F-score)
* TER (Translation Edit Rate)

The results are stored in:

```text
evaluation_scores.txt
```

---

## Tools and Technologies Used

* Google Colab
* Python 3
* Pandas
* Hugging Face Datasets
* Hugging Face Transformers
* SentencePiece
* SacreBLEU
* OpenPyXL

---

## Author

**Name:** Baiju Kumar

**Date:** 27 June 2026
