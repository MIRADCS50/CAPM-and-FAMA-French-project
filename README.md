# CAPM and Fama-French Asset Pricing & Econometric Analysis Toolkit

This repository contains a robust, end-to-end Python framework for financial econometric analysis, estimating both the single-factor **CAPM** and the multi-factor **Fama-French 3-Factor (FF3)** model using **Newey-West HAC** robust standard errors.

---

## 📁 Repository Structure & Files
- **`CAPM and FAMA French.ipynb`:** The core Jupyter notebook containing data ingestion, cleaning, HAC OLS regressions, residual analysis, volatility drag calculations, and advanced visualizations.
- **Visual Artifacts (`image.webp` through `image-(5).webp`):** Generated analytical plots including the Security Market Line (SML), annualized Jensen's Alpha bar charts with 95% HAC confidence intervals, and analytical documentation slides.

---

## 🚀 Key Features & Capabilities
1. **Automated Data Ingestion:** Fetches adjusted daily closing prices via `yfinance` and automatically downloads daily Fama-French factor data (`Mkt-RF`, `SMB`, `HML`, and Risk-Free Rate) directly from the Kenneth French Data Library.
2. **Custom HAC Estimation:** Implements Newey-West Heteroskedasticity and Autocorrelation Consistent (HAC) standard error matrices from scratch (using optimal lag selection) to yield reliable $t$-statistics and $p$-values.
3. **Comprehensive Performance Analytics:**
   - Evaluates Compounded Annual Growth Rate ($\text{CAGR}$) versus arithmetic mean returns to quantify **Volatility Drag**:
     $$\text{CAGR} \approx \bar{R} - \frac{1}{2}\sigma^2$$
   - Computes annualized Jensen's Alpha and performs rigorous statistical significance testing.
   - Performs **Factor Attribution** by examining market ($\beta_M$), size ($\beta_{\text{SMB}}$), and value ($\beta_{\text{HML}}$) loadings alongside $R^2$ improvements.
4. **Professional Visualizations:** Generates publication-ready SML plots and horizontal bar charts for annualized alphas with custom label offset handling to prevent text clipping on negative values.

---

## 📊 Econometric Framework

### 1. Capital Asset Pricing Model (CAPM)
The baseline time-series regression model is specified as:
$$R_{i,t} - R_{f,t} = \alpha_i + \beta_i (R_{m,t} - R_{f,t}) + \epsilon_{i,t}$$

2. Fama-French 3-Factor Model (FF3)

To control for size and value anomalies, the multi-factor extension is implemented:

$$R_{i,t} - R_{f,t} = \alpha_i + \beta_{i,M}(R_{m,t} - R_{f,t}) + \beta_{i,\text{SMB}}\text{SMB}_t + \beta_{i,\text{HML}}\text{HML}_t + \epsilon_{i,t}$$


---

## 🛠️ Getting Started

1. **Clone the repository:**
```bash
   git clone https://github.com/MIRADCS50/CAPM-and-FAMA-French-project.git
   cd CAPM-and-FAMA-French-project


