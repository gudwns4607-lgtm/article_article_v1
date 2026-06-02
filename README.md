# A Regime-Gated AI Framework for FinTech-Driven Risk Surveillance: Evidence from Korean Financial News Sentiment

This repository provides the official empirical source code, data preprocessing pipeline, and full replication package for the manuscript: 
**"A Regime-Gated AI Framework for FinTech-Driven Risk Surveillance: Evidence from Korean Financial News Sentiment"** (Working Paper / Under Peer Review).

---

## 🔬 Research Architecture & Core Empirical Overview

This research framework introduces an advanced FinTech-driven Early Warning System (EWS) utilizing a hybrid Natural Language Processing (NLP) pipeline combined with a supracritical volatility regime gate to monitor, quantify, and forecast systemic risks within the Korean stock market (KOSPI). 

By evaluating a high-density Korean financial text corpus spanning from 2020 to 2025, our methodology filters exactly **$N = 1,451$ effective daily trading observations** after rigorous lead-lag alignments ($t+1$) and asynchronous data trimming, completely eliminating data-snooping biases and operational endogeneity.

---

## 📊 Comprehensive Replication Matrix & Verification

To ensure full empirical transparency and compliance with open-science data verification, this repository includes a single, self-contained replication notebook (`Early_Warning_System_Replication.ipynb`). Executing this script reproduces every primary metric presented in the main manuscript with bit-wise mathematical identicality.

### Operational Verification Roadmap

| Section | Target Manuscript Element | Empirical Expected Output | Operational Status |
| :--- | :--- | :--- | :--- |
| **Section 1** | Data Retrieval & Preprocessing | Total Sample $N = 1,451$ trading days | ✅ Fully Aligned |
| **Section 2** | Volatility Regime-Gating | $Q_{75}$ Volatility Threshold Segmentation | ✅ Fully Aligned |
| **Section 3** | **Table 3** — Standardized Residuals | $z = 2.156$, $p = 0.031$ (Concurrent Dependency) | ✅ Fully Aligned ★ |
| **Section 4** | **Table 4 [C]** — Same-Day Logistic Regression | $\text{OR} = 22.771$, $\beta = 3.126$, $p = 0.130$ | ✅ Fully Aligned |
| **Section 5** | **Table 4 [P]** — Next-Day Predictive Logistic | $\text{OR} = 10.737$, $\beta = 2.374$, $p = 0.247$ | ✅ Fully Aligned |
| **Section 6** | **Table 6** — Placebo Permutation Test | $\text{OR}_{\text{obs}} = 11.064$, $p_{\text{perm}} = 0.129$ (1,000 Shuffles) | ✅ Fully Aligned |
| **Section 7** | Auditing Integration Matrix | Comprehensive Convergence Tracking (11/11 Items) | ✅ Fully Aligned |

---

## ⚙ Operational Instructions & Deployment

### 1. Cloud Execution (Google Colab)
The replication notebook features an automated, intelligent environmental sensor. You do not need to manually configure directory paths or upload dependencies:
1. Open the file `Early_Warning_System_Replication.ipynb` within Google Colab.
2. Select **Runtime -> Run All** (`Ctrl + F9`).
3. The integrated data parser will sequentially query local execution stacks, secure cloud-mapped storage virtual directories (`/content/drive/MyDrive/data/`), and automatically fall back to this public repository's secure raw content URL to stream the empirical source matrix (`logistic_regression_data.csv`).

### 2. Local Bare-Metal Setup
To run the analysis locally, initialize your statistical workspace with the following configuration:
```bash
pip install pandas numpy statsmodels scipy
python -m jupyter notebook Early_Warning_System_Replication.ipynb
