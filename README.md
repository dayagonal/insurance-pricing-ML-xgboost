# Insurance Risk Pricing
Система страхового ценообразования на основе машинного обучения для прогнозирования частоты и размера убытков и расчёта тарифа с целевым Loss Ratio.

## Competition Result

🥈 2nd Place — KBTU Risk Management Case Competition 2026

Built a complete insurance pricing pipeline that:

- predicted claim frequency and severity;
- recalibrated premiums;
- reduced portfolio Loss Ratio from 121.6% to 70%;
- passed stability and calibration tests.

_**Язык программирования Python!**_

This project builds an end-to-end machine learning pipeline to predict insurance risk and optimize pricing.

The model estimates:
- Claim probability (frequency)
- Claim severity (amount)
- Expected loss
- Optimal premium to achieve target loss ratio (70%)

The solution includes data cleaning, feature engineering, model training, calibration, and business-level pricing optimization.

## Business Problem

The initial insurance portfolio had a Loss Ratio of 121.6%, indicating that claim payments exceeded collected premiums.

The objective was to build a risk-based pricing system capable of reducing portfolio Loss Ratio to the target level of 70% while preserving risk differentiation across policyholders.

## Data Availability
The dataset is not publicly available due to confidentiality reasons.

## Disclaimer

This project was developed as part of a Company's case competition.
## Pipeline

### 1. Data Cleaning

- bonus-malus normalization
- vehicle year correction
- experience reconstruction
- outlier treatment
- missing value imputation


### 2. Feature Engineering

- risk indicators
- interaction features
- experience groups
- policy-level aggregations
- SCORE compression

### 3. Feature Selection

- Information Value (IV)
- Variance Inflation Factor (VIF)
- Tree-based importance

### 4. Modeling

#### Claim Frequency

- XGBoost Classifier
- LightGBM Classifier

#### Claim Severity

- XGBoost Regressor
- LightGBM Regressor

### 5. Calibration

- probability calibration
- severity bias correction
- holdout scaling

### 6. Pricing

- expected loss estimation
- premium recalculation
- target Loss Ratio optimization

## Model Performance

| Metric | XGBoost | LightGBM |
|----------|----------|----------|
| CV AUC | 0.821 | 0.820 |
| Gini | 0.642 | 0.640 |
| Train-Val GAP | 0.0479 | 0.0581 |
| Noise Correlation | 0.9806 | 0.9928 |
| Holdout LR Before Calibration | 65.71% | 88.31% |
| Holdout LR After Calibration | 70.00% | 70.02% |
