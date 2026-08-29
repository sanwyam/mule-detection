# Mule Account Detection System

An end-to-end machine learning system designed to detect **mule accounts** involved in suspicious financial activity. The system analyzes transaction behavior and network characteristics to identify accounts exhibiting patterns such as rapid fund movement, pass-through activity, fan-in, fan-out, and circular transactions.

The detection model is built using **XGBoost**, supported by behavioral and graph-based features such as **transaction velocity, pass-through ratio, PageRank, hub score, and authority score**. An interactive **Tableau dashboard** provides visual insights into account risk distribution and suspicious transaction patterns over time.

**Tech Stack:** Python · Pandas · NetworkX · XGBoost · Scikit-learn · Tableau

## Problem Statement

Financial fraud often involves **mule accounts** — accounts used to receive, transfer, or move illegally obtained funds while hiding the actual source of the money.

Traditional fraud detection systems often focus on individual transactions. However, mule accounts can exhibit suspicious behavior across **multiple transactions and interconnected accounts**.

This project aims to identify such accounts by analyzing:

- Account characteristics
- Incoming and outgoing transaction behavior
- Transaction velocity
- Fund pass-through behavior
- Account-to-account network relationships
- Graph-based centrality measures
- Known suspicious transaction patterns

---

## Solution

The system follows an end-to-end pipeline:

```text
Transaction & Account Data
          ↓
Data Preprocessing
          ↓
Transaction Network Construction
          ↓
Behavioral Feature Engineering
          ↓
Graph-Based Feature Engineering
          ↓
XGBoost Classification Model
          ↓
Mule / Non-Mule Prediction
          ↓
Risk Categorization
          ↓
Tableau Dashboard
