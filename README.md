# Network Prediction & Analysis

A machine learning project for **network performance time-series prediction** using **LSTM and XGBoost**, with an interactive **Streamlit dashboard** for visualization and analysis.

## Overview

The project predicts three network performance metrics:

- **PL**
- **PD**
- **PDV**

Two approaches are implemented and compared:

- **LSTM** — sequence-based time-series forecasting using the previous 5 time steps.
- **XGBoost** — regression using lagged features from the previous 3 time steps.

The resulting predictions are consolidated and presented through an interactive Streamlit dashboard.

## Workflow

```text
Network Data
     ↓
Preprocessing
     ↓
┌──────────────┬──────────────┐
│     LSTM     │   XGBoost    │
└──────────────┴──────────────┘
        ↓
   Predictions
        ↓
Model Comparison
        ↓
Streamlit Dashboard
```

## Project Structure

```text
Network-Prediction-Analysis/
│
├── src/
│   ├── pred/
│   │   ├── LSTM.ipynb
│   │   ├── XGB.ipynb
│   │   └── Comparision.ipynb
│   │
│   ├── Dashboard/
│   │   └── combined.py
│   │
│   └── data/
│       ├── Data1.csv
│       ├── lstm_result.csv
│       ├── xgb_result.csv
│       └── final_result.csv
│
├── requirements.txt
└── README.md
```

## Tech Stack

- Python
- Pandas & NumPy
- Scikit-learn
- TensorFlow / Keras
- XGBoost
- Plotly
- Streamlit
- Jupyter Notebook
- Git & GitHub

## Run Locally

### Install dependencies

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Start the dashboard

```bash
streamlit run src/Dashboard/combined.py
```

The application will open at:

```text
http://localhost:8501
```

## Key Components

**LSTM:** Uses sequential network data to forecast PL, PD, and PDV.

**XGBoost:** Uses lagged network metrics to generate predictions for the same variables.

**Streamlit Dashboard:** Provides interactive visualization of actual values, model predictions, and anomaly analysis.

## Collaboration

Developed collaboratively, covering machine-learning experimentation, prediction generation, result processing, and dashboard development.

## Purpose

This project demonstrates the application of **machine learning and time-series forecasting techniques to network performance analysis**.
