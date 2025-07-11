# 🧠 Dual-Attention Graph Neural Networks for Spatio-Temporal Crime Forecasting and Patrol Optimization

This repository contains the official implementation of our research paper submitted to **ICCCNT 2025**, titled:

> **"Dual-Attention Graph Neural Networks for Spatio-Temporal Crime Forecasting and Patrol Optimization"**

---

## 📌 Overview

Urban crime prediction is crucial for proactive policing and public safety planning. In this work, we present a novel **Dual-Attention Graph Neural Network (DA-GNN)** that:

- Models **spatial interactions** between urban districts using **Graph Attention Networks (GATs)**
- Captures **temporal dependencies** through a **Transformer-style self-attention encoder**
- Incorporates **external covariates** (weather, holidays, seasonality)
- Optimizes **patrol resource deployment** using **Quantum-behaved Particle Swarm Optimization (QPSO)**

The model is trained on district-level crime data from **Chicago (Jan–Mar 2023)** and demonstrates superior performance over classical baselines and deep learning models such as ARIMA, LSTM, and CNN–LSTM.

---

## 🔍 Key Features

- 📊 **Spatio-Temporal Forecasting**: Dual-attention mechanism jointly learns from spatial neighbors and temporal history
- 🌤 **Exogenous Features**: Weather data, holiday indicators, and seasonal cycles integrated as dynamic inputs
- 🧠 **Explainability**: Attention maps, spatial weights, and patrol risk scores visualized for ethical transparency
- 🚓 **QPSO Optimization**: Post-forecast optimization for patrol allocation based on predicted crime risk
- 📉 **Performance Metrics**: Evaluated using Mean Absolute Error (MAE), achieving significant improvements over existing models

---

## 🏗️ Architecture

  District Graph + Exogenous Features
                 │
            [Spatial GAT]
                 │
           ┌─────┴─────┐
      │          
[Temporal Encoder] ← Dual Attention →
                 │
           └─────┬─────┘
                 ↓
     [Forecasted Crime Risk]
                 ↓
   [QPSO-Based Patrol Optimizer]
