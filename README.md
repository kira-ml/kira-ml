<div align="center">
  <img src="assets/banner.png" alt="Ken Ira Lacson — Quantitative Research, Machine Learning, Portfolio Construction" width="100%" />
</div>

**Evaluation-first machine learning for financial decisions.**

[LinkedIn](https://www.linkedin.com/in/ken-ira-lacson-852026343/) · [Email](mailto:keniralacson@gmail.com) · [Kaggle](https://www.kaggle.com/keniralacson) · [GitHub](https://github.com/kira-ml)

---

> The binding constraint is usually the evaluation, not the model.

I build reproducible ML systems for financial decision-making: uncertainty-aware models, portfolio construction, execution costs, and the evaluation layer that decides whether a result is real. My default is baseline-first, point-in-time, net-of-cost, and pre-registered where the claim allows it.

| Research | Evaluation | Current |
|:---|:---|:---|
| Uncertainty · portfolio construction · risk | Point-in-time · net-of-cost · pre-registered | Advanced ML · conformal prediction |

---

## Flagship work

<sub>PROJECT 01 · RESEARCH</sub>

### Epistemic DRO

**Uncertainty-aware portfolio construction · pre-registered evaluation**

**Question.** Does ML epistemic uncertainty improve the tail-risk/return trade-off of a distributionally robust mean–CVaR portfolio, net of costs?

**Result.** One completed negative result, two pre-holdout stops, and an untouched 2025–2026 holdout. The paper also shows why the information gate itself needed a power audit.

`Python` `CVXPY` `LightGBM` `Conformal prediction` `Walk-forward`

[Paper](https://github.com/kira-ml/epistemic-dro/blob/main/paper/mini_paper.pdf) · [Repository](https://github.com/kira-ml/epistemic-dro)

<sub>PROJECT 02 · RESEARCH</sub>

### Robustfolio

**Evaluation benchmark for portfolio construction · null result**

**Question.** Does a robust portfolio method beat the best simple baseline after costs — once you account for having tried more than one method?

**Result.** Seven constructions, 168 out-of-sample months, and eight pre-registered gates. Both treatments fail. The comparator and the evaluation rule bind the verdict more than the model does.

`Python` `CVXPY` `Walk-forward` `Bootstrap inference`

[Working paper](https://github.com/kira-ml/robustfolio/blob/main/essays/robustfolio-working-paper.pdf) · [Repository](https://github.com/kira-ml/robustfolio)

<sub>PROJECT 03 · SYSTEM</sub>

### Execution Lab

**Execution costs and market impact · released system**

**Question.** Given a target portfolio and a rebalance, which execution schedule minimizes expected cost plus timing risk — and does the strategy ranking survive realistic costs?

**Result.** v0.1.0 · four schedules · 76 tests · capacity stress. Built to show what a flat 10-bps backtest assumption hides.

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

## Research pipeline

```mermaid
flowchart LR
    A["Point-in-time data"] --> B["ML + uncertainty"]
    B --> C["Risk model"]
    C --> D["Portfolio construction"]
    D --> E["Execution costs"]
    E --> F["Net-of-cost evaluation"]
    F --> G["Pre-registered verdict"]
    classDef paper fill:#F7F4EC,stroke:#C9C2B6,color:#14213D;
    classDef ink fill:#14213D,stroke:#14213D,color:#FFFFFF;
    class A,B,C,D,E,F paper;
    class G ink;
```

*The through-line across the projects: data → model → risk → portfolio → execution → evidence.*

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

| Layer | Tools |
|---|---|
| **Modeling** | Python · PyTorch · scikit-learn · LightGBM · probabilistic models |
| **Evaluation** | Walk-forward validation · bootstrap intervals · calibration · power analysis · deflated Sharpe |
| **Quantitative finance** | CVXPY · mean–CVaR · DRO · covariance shrinkage · factor models · execution costs |
| **Engineering** | pandas · NumPy · pytest · Git · GitHub Actions · Typst |

---

## Currently

Advanced Machine Learning · conformal prediction · power analysis · factor models

Open to ML/DS research internships and quantitative research roles.

---

<div align="center">

<sub>Research prototypes, not investment advice. No alpha or live-trading claims.</sub>

</div>
