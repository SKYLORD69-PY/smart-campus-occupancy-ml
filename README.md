# 🎓 Smart Campus Classroom Occupancy Prediction

A production-style machine learning pipeline that predicts classroom occupancy and overcrowding risk in a university environment. This project demonstrates ETL engineering, traditional ML modeling, SQL-backed storage, and an interactive dashboard.

---

## 🧠 Project Overview

Universities often allocate classrooms without accurate attendance forecasting. This leads to overcrowded rooms, underutilized venues, and inefficient scheduling.

This project builds a predictive system that:

- estimates classroom occupancy  
- detects overcrowding risk  
- visualizes campus utilization  
- supports real-time predictions  
- maintains a retrainable ML lifecycle  

The emphasis is not only model performance, but engineering a maintainable ML pipeline beyond notebooks.

---

## 🏗 Architecture

```
Data Generator → SQL Storage → Training Pipeline → Model Registry → Dashboard
```

This mirrors a real ETL-style ML production system:

**Extract** → synthetic campus data  
**Transform** → preprocessing + feature engineering  
**Load** → SQL + serialized models + dashboard deployment  

---

## 📊 Models Implemented

| Model | Purpose |
|------|---------|
Linear Regression | Attendance prediction |
Random Forest Regressor | Attendance prediction |
SVM Classifier | Overcrowding detection |

Evaluation includes:

- MAE / R²  
- Accuracy  
- Classification report  
- Confusion matrix  

---

## 📈 Dashboard Features

The interactive Streamlit dashboard provides:

- attendance analytics  
- venue utilization insights  
- overcrowding risk visualization  
- model performance metrics  
- confusion matrix display  
- live prediction interface  

Users can input class parameters and instantly receive safety predictions.

---

## 🔄 Model Lifecycle

The system supports periodic retraining:

- new data appended  
- model retrained  
- new version stored  
- dashboard loads latest model  
- previous versions archived  

This simulates real-world ML maintenance workflows.

---

## 📦 Dataset Policy

No CSV datasets are stored in this repository.

A reproducible generator script is provided:

```
data_generator/generate_data.py
```

Running this script recreates the full dataset.

This ensures reproducibility and complies with repository size rules.

---

## ⚙️ Quick Start

Install dependencies:

```
pip install -r requirements.txt
```

Generate dataset:

```
python data_generator/generate_data.py
```

Train models:

```
python training/train_models.py
```

Run dashboard:

```
streamlit run dashboard/app.py
```

---

## 📁 Repository Structure

```
data_generator/    dataset synthesis
database/          SQL ingestion scripts
training/          preprocessing + model training
models/            model registry metadata
dashboard/         Streamlit application
notebooks/         experimentation
```

---

## 🧪 ETL Justification

This project implements an ETL-style ML pipeline:

Extract → synthetic academic data  
Transform → feature engineering  
Load → SQL + model deployment  

This architecture mirrors production ML systems.

---


