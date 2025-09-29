# Naive Bayes Classifier for Fake News Recognition

This repository contains the implementation of a **Multinomial Naive Bayes (MNB) Classifier** in R for the task of Fake News Text Classification.  
The project focuses on applying core **Natural Language Processing (NLP)** techniques to prepare textual data and evaluate the classifier's performance on two distinct datasets: a complex multiclass problem and a simpler binary classification problem.

---

## Project Goal
The primary objective is to implement and test a Multinomial Naive Bayes classifier on social media text data to:

- Distinguish between different levels of truthfulness (**multiclass**).  
- Identify articles as **reliable** or **unreliable** (**binary**).

---

## Datasets
Two public datasets from Kaggle were used for training and evaluation:

### Multiclass Dataset
- **Task:** Predict one of six truthfulness labels.  
- **Labels:**  
  - Barely-True (0)  
  - False (1)  
  - Half-True (2)  
  - Mostly-True (3)  
  - Not-Known (4)  
  - True (5)  
- **Source:** [Fake News Content Detection - Kaggle](https://www.kaggle.com/datasets/ruchi798/fake-news-detection)

### Binary Dataset
- **Task:** Predict reliability (0 or 1).  
- **Labels:**  
  - Unreliable (0)  
  - Reliable (1)  
- **Source:** [Fake News: Build a System to Identify Unreliable News Articles - Kaggle](https://www.kaggle.com/c/fake-news)

---

## Project Structure
- **`Elaheh Ahmadieslamloo_NaiveBC.ipynb`**: Main Jupyter Notebook containing the R implementation, preprocessing, training, and evaluation.
- **`README.md`**: Project overview file (this document).  

---

## Prerequisites
To run this project, you need:

- R (version 4.x or later recommended)  
- RStudio (optional, but recommended)  
- Jupyter Notebook or JupyterLab (with the R kernel installed)  

---

## Setup and Installation

### 1. Clone the repository
```bash
git clone https://github.com/EliAhmadies/Naive-Bayes-classifier-for-Fake-News-recognition.git
cd Naive-Bayes-classifier-for-Fake-News-recognition
```

### 2. Install R Packages
Open **R** or **RStudio** and install the required packages by running:

```r
install.packages(c("tm", "dplyr", "e1071", "caret", "ggplot2"))
```

### 3. Install R Kernel for Jupyter (if needed)

In **R**, run:

```r
install.packages("IRkernel")
IRkernel::installspec()
```

## Methodology & Steps

The notebook follows a structured workflow to prepare the data and train the model:

1. **Data Acquisition and Splitting**  
   Load the datasets and divide them into training, validation, and test sets.

2. **Tokenization and Cleaning**  
   Convert text to lowercase, split into tokens, and remove common English stop words (e.g., "the," "a," "is").

3. **Token Normalization**  
   Standardize tokens using stemming, lemmatization, or simple mappings so that similar words are treated as equivalent.

4. **Vocabulary Building & Feature Selection**  
   Construct a Document-Term Matrix (DTM) and apply feature selection techniques, such as removing sparse or low-frequency terms.

5. **Model Training**  
   Train the **Multinomial Naive Bayes (MNB)** classifier on the processed features.

6. **Evaluation**  
   Measure performance using metrics such as **Accuracy** and **Confusion Matrix** for both multiclass and binary classification tasks.

---

## Key Findings

The evaluation highlighted clear differences in model performance depending on task complexity:

- **Multiclass Classification**  
  - Accuracy was relatively low (**~22.3%**) due to the fine-grained nature of the six truthfulness labels and limited dataset size.  
  - This underscores the difficulty of multiclass text classification.

- **Binary Classification**  
  - Accuracy improved significantly (**~61.1%**), showing that the MNB model performs better on simpler binary classification tasks.

---

## References

1. C. D. Manning, *Introduction to Information Retrieval*, Chapter 13: Text Classification and Naive Bayes, Cambridge University Press, 2008.  
2. [Fake News Content Detection - Kaggle](https://www.kaggle.com/datasets/ruchi798/fake-news-detection)  
3. [Fake News: Build a System to Identify Unreliable News Articles - Kaggle](https://www.kaggle.com/c/fake-news)  

