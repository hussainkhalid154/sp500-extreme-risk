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

## 📈 Model Diagnostics & Visualizations

### **1. Distribution of Losses**
![Distribution of Losses](images/distribution_of_losses.png)
*The empirical distribution of S&P 500 daily losses (1986-2025) shows right-skewed behavior with a heavy tail, indicating frequent moderate losses and rare extreme events.*

### **2. Distribution Fit (GPD vs Empirical)**
![Distribution Fit](images/distribution_fit.png)
*Comparison between empirical exceedances (blue) and fitted Generalized Pareto Distribution (orange). The GPD closely matches the empirical distribution, especially in the moderate tail region.*

### **3. QQ Plot - GPD Fit Assessment**
![QQ Plot](images/qq_plot.png)
*Quantile-Quantile plot comparing empirical quantiles against theoretical GPD quantiles. Points following the diagonal line indicate good fit. The slight upward curvature in the extreme tail suggests the model may slightly underestimate the heaviest losses.*

### **4. Tail Probability Comparison**
![Tail Probability Comparison](images/tail_probability_comparison.png)
*Log-scale comparison of tail probabilities. The empirical survival function (blue) and GPD model (orange) show excellent agreement for probabilities > 0.01, with slight divergence in the extreme tail (probabilities < 0.001).*

### **5. Tail Plot (Log Scale)**
![Tail Plot](images/tail_plot.png)
*Log-scale visualization of the tail region, highlighting the power-law decay characteristic of heavy-tailed distributions. The linear trend in the log-log plot confirms the GPD's appropriateness.*

### **6. Return Level Plot**
![Return Level Plot](images/return_level_plot.png)
*Return levels for different return periods (10 to 1000 days). The smooth extrapolation beyond observed data provides confidence in extreme quantile estimates, with 1000-day return level (~99.9% VaR) around 9.7%.*

### **7. Mean Excess Plot for Threshold Selection**
![Mean Excess Plot](images/mean_excess_plot.png)
*Mean excess vs threshold plot used for optimal threshold selection. The chosen threshold (2.93% loss, 97.1th percentile) represents the point where the mean excess stabilizes, indicating the onset of extreme behavior.*

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
