# Default-Probabilities

## CRE Probability of Default Scoring Model

### Project Overview

This project creates a simulated commercial real estate loan dataset and applies a probability-of-default scoring framework using Python, NumPy, and pandas.

### Tools Used

- Python
- NumPy
- pandas
- Jupyter Notebook / Google Colab

### Dataset

The project generates a simulated loan tape with 1,000 commercial real estate loans.

#### Fields Included

- Loan ID
- Property Type
- Loan-to-Value Ratio
- Debt Service Coverage Ratio
- Occupancy
- Sponsor Risk Score
- Market Stress Index
- Loan Age
- Property Risk Flag

### Methodology

The model creates a loan-level risk score by combining multiple credit-risk drivers.

### Core Formula

```python
Def_prob = 1 / (1 + np.exp(-risk_score))
