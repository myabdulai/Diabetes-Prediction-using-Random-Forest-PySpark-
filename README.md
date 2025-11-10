# 🧠 Diabetes Prediction using Random Forest (PySpark)

[![Apache Spark](https://img.shields.io/badge/Apache%20Spark-3.5.0-orange?logo=apachespark)](https://spark.apache.org/)
[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)](https://www.python.org/)
[![Hadoop](https://img.shields.io/badge/Hadoop-Cluster-yellow?logo=apache)](https://hadoop.apache.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📘 Project Overview
This project demonstrates the use of **Apache Spark MLlib** to build a **Random Forest classification model** for predicting diabetes outcomes using population health data.  
It leverages **distributed computing** across a two-node Spark cluster (`hadoop1` and `hadoop2`) to showcase scalable machine learning for health informatics and population analytics.

The main objective is to illustrate how Spark’s in-memory processing and parallelism can accelerate healthcare data science workflows while maintaining model interpretability and reproducibility.

---

## ⚙️ Methodology

1. **Data Loading & Preparation**
   - CSV data loaded via SparkSession.
   - Schema inferred automatically with `inferSchema=True`.
   - Features assembled using `VectorAssembler` from Spark MLlib.

2. **Model Training**
   - Implemented a `RandomForestClassifier` to predict diabetes likelihood.
   - Train-test split (80/20) for performance validation.
   - Dynamic executor allocation enabled for efficient cluster utilization.

3. **Evaluation**
   - Evaluated using Spark’s built-in evaluators for:
     - Accuracy  
     - Precision  
     - Recall  
     - F1-score  
     - ROC-AUC

---

## 📊 Model Performance

| Metric | Value |
|:--------|:------:|
| **Accuracy** | 0.8638 |
| **Precision** | 0.8690 |
| **Recall** | 0.9908 |
| **F1-score** | 0.8176 |
| **ROC-AUC** | 0.8209 |

**Interpretation:**  
The Random Forest model achieved **86% accuracy** and **very high recall (99%)**, indicating strong sensitivity in identifying diabetic cases.  
This performance is ideal for public health screening, where minimizing false negatives is critical.  
The ROC-AUC of 0.82 further confirms the model’s robust discrimination between diabetic and non-diabetic individuals.

---

## 🚀 Technologies Used

- **Apache Spark 3.5.0** — MLlib for distributed machine learning  
- **Hadoop HDFS** — Storage for large-scale health data  
- **PySpark** — Python API for Spark ML  
- **Fedora Linux** — Virtualized on VMware Workstation  
- **Python 3.11** — For model orchestration and evaluation  

---
## Data source:
https://www.kaggle.com/datasets/mahletbegashaw/diabetes-binary-health-indicators-brfss2015-csv
