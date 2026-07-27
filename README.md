# Default-Probabilities
CRE Probability of Default Scoring Model
Project Overview

This project creates a simulated commercial real estate loan dataset and applies a probability-of-default scoring framework using Python, NumPy, and pandas. The model generates loan-level credit risk inputs, assigns property-sector risk flags, calculates a weighted credit risk score, and converts that score into an estimated default probability.

The purpose of this project is to demonstrate how CRE loan risk drivers can be structured into a portfolio surveillance framework. The model uses common underwriting and credit-risk variables such as loan-to-value ratio, debt service coverage ratio, occupancy, sponsor risk, market stress, property type, and loan age.

Tools Used
Python
NumPy
pandas
Jupyter Notebook / Google Colab
Dataset

The project generates a simulated loan tape with 1,000 commercial real estate loans. Each loan includes the following fields:

Loan ID
Property Type
Loan-to-Value Ratio
Debt Service Coverage Ratio
Occupancy
Sponsor Risk Score
Market Stress Index
Loan Age
Property Risk Flag

The property types include:

Industrial
Multifamily
Retail
Office
Hotel

Each property type is assigned a risk flag to reflect differences in sector-level credit risk. Industrial receives the lowest property-risk flag, while hotel and office properties receive higher risk flags based on greater sensitivity to occupancy, economic cycles, and market stress.

Methodology

The model creates a loan-level risk score by combining multiple credit-risk drivers. Higher LTV, lower DSCR, lower occupancy, elevated sponsor risk, higher market stress, riskier property type, and loan age contribute to the final score.

Random noise is added to make the simulated dataset more realistic and to avoid perfectly deterministic outcomes. The risk score is then transformed into a probability of default using a logistic function.

The logistic transformation converts each loan’s risk score into a probability between 0% and 100%.

Core Formula
Def_prob = 1 / (1 + np.exp(-risk_score))

This converts the raw risk score into an estimated default probability.

Key Outputs

The project produces:

A 1,000-loan simulated CRE loan tape
Summary statistics for credit-risk variables
Property type distribution
Property-level risk flags
Loan-level default probability estimates
Example Use Cases

This framework can support:

CRE loan surveillance
Credit-risk ranking
Portfolio segmentation
Early-warning model development
Stress testing preparation
Probability-of-default modeling practice
Future Enhancements

Potential future enhancements include adding machine-learning models, calibration testing, validation metrics, decile analysis, precision and recall testing, portfolio-level expected loss, and watchlist optimization.
