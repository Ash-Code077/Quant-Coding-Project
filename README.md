# Quant-Coding-Project: Hybrid Market Signal Model

## Overview

This project explores the development of a hybrid quantitative model for stock price prediction by combining:

- Sentiment-based signals (behavioral factors)
- Structural volatility signals (mathematical/market dynamics)

The goal is to investigate when different factors dominate market behavior and how they can be combined into a unified predictive framework.

---

## Core Idea

Markets are driven by two primary forces:

1. **Behavioral (Sentiment)**
2. **Structural (Market Dynamics / Volatility)**

This project attempts to model both and dynamically weight them based on market conditions.

---

## Model Framework

Final signal:

$S_{final} = w1 * S_{sentimental} + w2 * S_{mathematical}$

Where:
- $S_{sentimental}$: sentiment-based signal
- $S_{mathematical}$: structural volatility signal
- w1, w2: adaptive weights based on market regime

---

## Research Goals

- Determine whether sentiment or structural factors better explain price movements
- Develop a structural volatility metric based on price trajectory geometry
- Test regime-dependent behavior in financial markets
- Build a foundation for a backtestable trading strategy

---

## Status

This is an active research project. Current focus:
- Defining mathematical features
- Building testable hypotheses
- Preparing for empirical validation

---

## Next Steps

- Implement features in Python
- Backtest signals on historical data
- Evaluate predictive performance across assets
