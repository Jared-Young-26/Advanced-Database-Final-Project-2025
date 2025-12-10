# 📊 Advanced Database Project — Diabetes Indicator Analysis  
### CSV vs SQLite vs Mongita Performance + Machine Learning Classification

This project compares how three different data-processing approaches—**CSV (Pandas)**, **SQLite**, and **Mongita**—perform when executing analytical queries on a 100,000-record diabetes dataset.  
It also implements a full machine learning pipeline to classify diabetes using **Logistic Regression**, a **Neural Network**, and an **SVM**.

The notebook implements a complete workflow:

**CSV → SQLite → Mongita → Statistics → ML Models → Summary**

---

## 🚀 Features

### 🔹 Database Engine Comparison
- Fast CSV queries using Pandas
- SQLite queries (unindexed vs indexed)
- Query plan introspection using `EXPLAIN QUERY PLAN`
- Mongita document-based queries (unindexed vs indexed)

### 🔹 Statistical Exploration
- Summary statistics (`df.describe()`)
- Class distribution for `diagnosed_diabetes`
- Numeric correlation heatmap

### 🔹 Machine Learning
- One-hot encoding of categorical data
- Feature scaling using `StandardScaler`
- Models:
  - Logistic Regression
  - Keras Neural Network
  - Support Vector Machine (linear kernel)
- Accuracy, precision, recall, confusion matrix

---

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/Jared-Young-26/Advanced-Database-Final-Project-2025.git
cd Advanced-Database-Final-Project-2025
```
### 2. Create a virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate        # macOS/Linux
.\.venv\Scripts\activate         # Windows
```
### 3. Install dependencies
```bash
pip install -r requirements.txt
```

## ▶️ Running the Project
### Run the Jupyter notebook
```bash
jupyter notebook
```
Open the provided notebook and run all cells in sequence.

### Run the Python script
```bash
python notebook.py
```

Running the script performs:
* Data loading
* Statistical summaries
* CSV/Pandas query timing
* SQLite loading + query timing
* SQLite indexing + re-timing
* Mongita querying
* ML model training (LogReg, NN, SVM)
* Final printed summary

## 🧠 High-Level Process Overview
### 1. Load Dataset

Imports the CSV, displays sample rows, and verifies schema.

### 2. Statistical Exploration

Computes descriptive statistics and visualizes correlations among numeric features.

### 3. CSV Query Benchmarking

Measures performance of typical analytical queries using Pandas.

### 4. SQLite Pipeline

Creates a relational table from the dataset, times several SQL queries, adds indexes, and reruns those queries to compare performance.

### 5. Mongita Pipeline

Stores a document-version of the dataset and runs equivalent queries to illustrate NoSQL-style filtering and indexing differences.

### 6. Machine Learning

Preprocesses data (encoding + scaling), trains three classification models, and prints performance metrics.

### 7. Summary

A consolidated list of everything completed in the notebook/script.