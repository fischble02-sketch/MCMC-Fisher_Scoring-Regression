# MCMC-Fisher_Scoring-Regression
## Overview
This project implements logistic and Poisson regression from scratch without using high-level ML libraries. Parameter estimation is performed using Fisher Scoring and MCMC methods. Two real-world datasets are analyzed to compare frequentist and Bayesian approaches.
## Content
| File                    | Description |
|-------------------------|------------|
| Hospital.csv            | Dataset containing hospital patient information |
| CreditCard.csv          | Dataset containing credit card application data |
| Code_Fisher_MCMC.ipynb  | Jupyter notebook implementing logistic (CreditCard) and Poisson (Hospital) regression |
| Dataset_explanation.txt | Information on datasets |

## Methods
### Fisher Scoring / IRLS (Logistic & Poisson)
### MCMC 
- Sampler: random-walk Metropolis-Hastings  
- Proposal: Gaussian random-walk proposal  
- Target acceptance: 0.5
- Convergence criterion: ||β^(t+1) − β^(t)|| < tol

### Diagnostics
- Trace plots for posterior samples  
- Autocorrelation function (ACF)  
- Acceptance rate monitoring  

## Results
- Fisher Scoring converges within 6-13 iterations
- Observed MCMC acceptance rate after burn-in ≈ 0.45
- Posterior means closely match MLE results obtained via Fisher Scoring (and built-in function)

## How to run
```bash
pip install -r requirements.txt
