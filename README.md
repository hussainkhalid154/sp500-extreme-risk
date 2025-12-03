# # 📊 S&P 500 Extreme Risk Model - Bayesian EVT Analysis

**Author:** [HUSSAIN KHALID]  
**Email:** [hussainkhalid1544@gmail.com]  
**LinkedIn:** [https://www.linkedln.com/in/hussainkhalid1544]  
**GitHub:** [https://github.com/hussainkhalid154]

---

## 🔬 Research Project: Extreme Value Theory for S&P 500

This repository contains my implementation of a **Bayesian Extreme Value Theory (EVT) model** for analyzing extreme daily losses in the S&P 500 index from 1986-2025. The model uses **Peaks-Over-Threshold methodology** with **Generalized Pareto Distribution** and **Hamiltonian Monte Carlo (MCMC)** for Bayesian inference.

### 🎯 **Key Contributions:**
1. **Optimal Threshold Selection** (97.1th percentile - 2.90% loss threshold)
2. **Bayesian Parameter Estimation** (ξ = 0.4212, σ = 0.0090)
3. **Risk Metrics with Uncertainty** (VaR & ES with 95% HDI intervals)
4. **Complete Diagnostic Framework** (QQ plots, tail probability, return level plots)

---

## 📊 **Key Results (S&P 500: 1986-2025)**

| Risk Metric | Estimate (95% HDI) | Interpretation |
|------------|-------------------|----------------|
| **Tail Index (ξ)** | 0.421 (0.173 - 0.675) | Heavy-tailed distribution |
| **99% VaR** | 4.13% (3.87% - 4.43%) | Daily loss threshold (1-in-100 days) |
| **99.9% VaR** | 9.71% (7.59% - 13.43%) | Extreme loss threshold (1-in-1000 days) |
| **99.9% ES** | 17.71% (10.19% - 38.44%) | Average extreme loss (Black Monday-like events) |

---

## 🚀 **Quick Start**

```bash
# Clone repository
git clone https://github.com/hussainkhalid154/sp500-extreme-risk.git
cd sp500-extreme-risk

# Install dependencies
pip install -r requirements.txt

# Run full analysis
python scripts/run_analysis.py

# Or explore notebooks
jupyter notebook notebooks/sp500-extreme-risk
