<div align="center">

# Ken Ira Lacson

**Machine Learning & Data Science · Quantitative Research**

<sub>Manila, Philippines · BSCS Machine Learning Track, National University Manila</sub>

[LinkedIn](https://www.linkedin.com/in/ken-ira-lacson-852026343/) · [Email](mailto:keniralacson@gmail.com) · [Kaggle](https://www.kaggle.com/keniralacson) · [GitHub](https://github.com/kira-ml)

</div>

---

> The binding constraint is usually the evaluation, not the model.

I build reproducible ML systems for financial decision-making: uncertainty-aware models, portfolio construction, execution costs, and the evaluation layer that decides whether a result is real. My default is baseline-first, point-in-time, net-of-cost, and pre-registered where the claim allows it.

---

## Flagship work

### 01 — Epistemic DRO

**Uncertainty-aware portfolio construction · pre-registered evaluation**

A pre-registered test of whether ML epistemic uncertainty improves a distributionally robust mean–CVaR portfolio, net of costs. One completed negative result, two pre-holdout stops, and an untouched 2025–2026 holdout. The paper also shows why the information gate itself needed a power audit.

**Result** — one completed negative result · two pre-holdout stops · zero holdout touches.

`Python` `CVXPY` `LightGBM` `Conformal prediction` `Walk-forward`

[Paper](https://github.com/kira-ml/epistemic-dro/blob/main/paper/mini_paper.pdf) · [Repository](https://github.com/kira-ml/epistemic-dro)

### 02 — Robustfolio

**Evaluation benchmark for portfolio construction · null result**

Seven portfolio constructions, 168 out-of-sample months, and eight pre-registered gates. Both treatments fail. The project makes the case that the comparator and the evaluation rule bind the verdict more than the model does.

**Result** — 18 US ETFs · 168 months · 8 gates · both treatments fail.

`Python` `CVXPY` `Walk-forward` `Bootstrap inference`

[Working paper](https://github.com/kira-ml/robustfolio/blob/main/essays/robustfolio-working-paper.pdf) · [Repository](https://github.com/kira-ml/robustfolio)

### 03 — Execution Lab

**Execution costs and market impact · released system**

A transparent laboratory for the cost assumptions hidden inside a backtest: spread, commission, square-root impact, and timing risk across immediate, TWAP, VWAP, and POV schedules. Built to show when a strategy ranking survives realistic costs — and when it does not.

**Result** — v0.1.0 · 4 schedules · 76 tests · capacity stress.

`Python` `CLI` `Cost modeling` `Capacity analysis`

[Repository](https://github.com/kira-ml/execution-lab) · [Method](https://github.com/kira-ml/execution-lab/blob/main/docs/METHOD.md)

**Synthesis:** [Two nulls, one evaluation problem](https://github.com/kira-ml/robustfolio/blob/main/essays/two-nulls-one-evaluation-problem.md) — what the two research projects teach about comparator choice, power, gate error rates, and holdout discipline.

---

## How I work

| Principle | In practice |
|---|---|
| **Baseline first** | A complex model must beat a simple regularized baseline on identical splits. |
| **Point-in-time or not at all** | No random splits on temporal data; features are lagged; costs are net. |
| **Pre-register the decision rule** | Comparator, metric, gates, and holdout are fixed before the result. |
| **Report the null** | A clean negative result is a successful outcome if the protocol holds. |

---

## Selected ML systems

| Project | What it demonstrates |
|---|---|
| [Delayed-Label Fraud Decisioning](https://github.com/kira-ml/delayed-label-fraud-decisioning) | Cost-sensitive fraud policy under delayed, censored labels; chronological splits, a calibration gate, and a deployed Streamlit app. The policy reduces realized cost by 22.3% against the strongest simple rule. |
| [Real-Time Fraud Detection](https://github.com/kira-ml/fraud-detection-real-time) | Leakage-free temporal pipeline with LightGBM; 0.7925 test PR-AUC at 0.03% FPR, with a Flask/Postgres audit trail. |
| [MoE Factor Timing v2](https://github.com/kira-ml/moe-factor-timing-v2) | Probabilistic regime-aware factor allocation across six US equity factors; 627 out-of-sample decisions and a 248-month holdout. Inconclusive, with a DOI. |
| [MAE Microstructure Denoising](https://github.com/kira-ml/mae-microstructure-denoising) | Self-supervised denoising of bid–ask noise with causal normalization; synthetic study with explicit limitations. |

---

## Toolkit

**Modeling** · Python, PyTorch, scikit-learn, LightGBM, probabilistic models  
**Evaluation** · walk-forward validation, bootstrap intervals, calibration, power analysis, deflated Sharpe  
**Quantitative finance** · CVXPY, mean–CVaR, DRO, covariance shrinkage, factor models, execution costs  
**Engineering** · pandas, NumPy, pytest, Git, GitHub Actions, Typst

---

## Currently

Advanced Machine Learning · conformal prediction · power analysis · factor models

Open to ML/DS research internships and quantitative research roles.

---

<div align="center">

<sub>Research prototypes, not investment advice. No alpha or live-trading claims.</sub>

</div>
