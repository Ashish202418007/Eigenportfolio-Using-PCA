# Eigenportfolio: PCA-based Portfolio Optimization

This project uses **Principal Component Analysis (PCA)** to construct *eigenportfolios* from asset returns, aiming to improve diversification and risk-adjusted performance over market benchmarks.

---

## Key Results

- **Best Sharpe Eigenportfolio**  
   - CAGR = **72.64%**
   - Volatility = **35.47%**
   - Sharpe = **1.77**

- **Best Custom Metric Eigenportfolio**  
   - CAGR = **72.64%**
   - Volatility = **35.47%**
   - Sharpe = **1.77**

- **Dimensionality Reduction**  
  - ~200 principal components explain **99% of the variance** in a dataset of **419 assets**.

---

## Methodology

The pipeline executes the following steps:

1. **Normalize Returns**  
   Daily asset returns are normalized to have zero mean and unit variance.

2. **Covariance & PCA**  
   - Build a covariance matrix from normalized returns.  
   - Perform eigen decomposition to extract principal components (eigenvectors and eigenvalues).

3. **Construct Eigenportfolios**  
   Portfolio weights are derived from the eigenvectors.

4. **Evaluation**  
   Each eigenportfolio is evaluated based on:
   - **Compound Annual Growth Rate (CAGR)**
   - **Volatility**
   - **Sharpe Ratio**  
   A custom metric `(Return × Sharpe)` is also used to identify high-return, risk-adjusted portfolios.
