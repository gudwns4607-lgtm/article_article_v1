# A Regime-Gated AI Framework for FinTech-Driven Risk Surveillance: Evidence from Korean Financial News Sentiment

This repository provides the official empirical source code, automated data preprocessing pipelines, and the complete replication package for the manuscript: 
**"A Regime-Gated AI Framework for FinTech-Driven Risk Surveillance: Evidence from Korean Financial News Sentiment"** (Working Paper / Under Peer Review).

---

## 🔬 Core Empirical Overview & Research Architecture

This research framework introduces an advanced FinTech-driven Early Warning System (EWS) that integrates a hybrid Natural Language Processing (NLP) pipeline with a supracritical volatility regime gate. The architecture is designed to monitor, quantify, and forecast systemic macro-financial risks within the Korean stock market (KOSPI).

By evaluating a high-density, longitudinal financial corpus spanning from 2020 to 2025, the empirical pipeline filters exactly **N = 1,451 effective daily trading observations**. This structural sample alignment is achieved through rigorous lead-lag matching (t+1) and asynchronous data trimming, effectively isolating the framework from data-snooping biases and operational endogeneity.

---

## 📊 Comprehensive Replication Matrix & Empirical Verification

To guarantee full scientific transparency and compliance with open-science replication standards, this repository provides a unified, self-contained replication notebook (**Replication_Notebook.ipynb**). Executing this statistical script reproduces every primary metric reported in the manuscript's tables with bit-wise mathematical identicality.

### Operational Verification Roadmap

| Section | Target Manuscript Element | Empirical Expected Output | Operational Status |
| :--- | :--- | :--- | :--- |
| **Section 1** | Data Retrieval & Preprocessing | Total Sample N = 1,451 trading days | ✅ Fully Aligned |
| **Section 2** | Volatility Regime-Gating | Q75 Volatility Threshold Segmentation (N = 363) | ✅ Fully Aligned |
| **Section 3** | **Table 3** — Standardized Residuals | z = 2.156, p = 0.031 (Contemporaneous Co-occurrence) | ✅ Fully Aligned ★ |
| **Section 4** | **Table 4 [C]** — Same-Day Logistic Regression | OR = 22.771, beta = 3.126, p = 0.130 | ✅ Fully Aligned |
| **Section 5** | **Table 4 [P]** — Next-Day Logistic Regression | OR = 10.737, beta = 2.374, p = 0.247 | ✅ Fully Aligned |
| **Section 6** | **Table 6** — Placebo Permutation Test | OR_obs = 11.064, p_perm = 0.129 (1,000 Shuffles) | ✅ Fully Aligned |
| **Section 7** | Auditing Integration Matrix | Comprehensive Convergence Tracking (11/11 Statistics) | ✅ Fully Aligned |

---

## 💡 Methodological Note on Target Risk Vectors

To preserve strict econometric boundaries and prevent endogeneity loops, the empirical package parameterizes risk outcomes via two distinct target vectors:
* **`MarketDown_C`** ($t$): Parameterized as $1$ if $\text{KOSPI Return}_t < 0$ (Contemporaneous market contraction). Utilized in **Table 3** & **Table 4 [C]**.
* **`MarketDown_P`** ($t+1$): Parameterized as $1$ if $\text{KOSPI Return}_{t+1} < 0$ (Forward-looking next-day risk surge). Utilized in **Table 4 [P]** & **Table 6** (Placebo test).

> ⚠️ **Econometric Design Feature**: To completely eliminate mechanical loop inference and severe multicollinearity, the concurrent vector $\text{KOSPI Return}_t$ is explicitly omitted from the set of predictors within the same-day conditional regression pipeline (**Table 4 [C]**).

---

## 📬 Support & Blind-Review Compliance

* **Technical Inquiries**: Please open a GitHub **Issue** or submit a **Pull Request** directly within this anonymous repository for secondary metadata or verification support.
* **Double-Blind Policy Compliance**: In strict adherence to the target journal's peer-review guidelines, all author profiles, institutional affiliations, and direct correspondence metadata are intentionally redacted during the evaluation phase. Complete repository ownership and com
