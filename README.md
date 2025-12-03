# 📊 S&P 500 Extreme Risk Model - Bayesian EVT Analysis

**Author**: Hussain Khalid  
**Email**: hussainkhalid1544@gmail.com  
**LinkedIn**: [linkedin.com/in/hussainkhalid1544](https://linkedin.com/in/hussainkhalid1544)  
**GitHub**: [github.com/hussainkhalid154](https://github.com/hussainkhalid154)  

---

## 🔬 Research Project: Extreme Value Theory for S&P 500

This repository contains my implementation of a **Bayesian Extreme Value Theory (EVT)** model for analyzing extreme daily losses in the S&P 500 index from 1986-2025. The model uses **Peaks-Over-Threshold methodology** with **Generalized Pareto Distribution** and **Hamiltonian Monte Carlo (MCMC)** for Bayesian inference.

### 🎯 Key Contributions:
- **Optimal Threshold Selection** (97.1th percentile - 2.90% loss threshold)
- **Bayesian Parameter Estimation** (ξ = 0.4212, σ = 0.0090)
- **Risk Metrics with Uncertainty** (VaR & ES with 95% HDI intervals)
- **Complete Diagnostic Framework** (QQ plots, tail probability, return level plots)
- **Production-Ready Model** with convergence validation (R_hat=1.0, ESS>4000)

---

## 📊 Key Results (S&P 500: 1986-2025)

| Risk Metric | Estimate (95% HDI) | Interpretation |
|-------------|-------------------|----------------|
| **Tail Index (ξ)** | 0.421 (0.173 - 0.675) | Heavy-tailed distribution |
| **99% VaR** | 4.13% (3.87% - 4.43%) | Daily loss threshold (1-in-100 days) |
| **99.9% VaR** | 9.71% (7.59% - 13.43%) | Extreme loss threshold (1-in-1000 days) |
| **99.9% ES** | 17.71% (10.19% - 38.44%) | Average extreme loss (Black Monday-like) |

---

## 🚀 Quick Start

### **Method 1: Google Colab (Recommended)**
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hussainkhalid154/S&P-500-Extreme-Risk/blob/main/S&P%20500%20Extreme%20Risk.ipynb)

1. Click the Colab badge above
2. Run all cells (Runtime → Run all)
3. No installation required!

### **Method 2: Local Installation**
```bash
# Clone repository
git clone https://github.com/hussainkhalid154/S&P-500-Extreme-Risk.git
cd S&P-500-Extreme-Risk

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter notebook
jupyter notebook "S&P 500 Extreme Risk.ipynb"
