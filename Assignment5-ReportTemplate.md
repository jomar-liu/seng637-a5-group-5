**SENG 637- Dependability and Reliability of Software Systems***

**Lab. Report \#5 – Software Reliability Assessment**

| Group \#:      |  5  |
| -------------- | --- |
| Student Names: | Lawrence |
|                | Kwesi |
|                | Joe |
|                | Zhanzhi |

# Introduction
This lab analyzes integration test failure data using two reliability assessment approaches: Reliability Growth Testing and Reliability Demonstration Charts (RDC). Reliability growth testing models how failure intensity changes over time as faults are detected and fixed, while RDC evaluates whether the system meets specified reliability targets. Together, these methods provide both analytical insight and decision support for assessing the reliability of the system under test (SUT).
# 

# Assessment Using Reliability Growth Testing 
Reliability growth testing helps estimate time, cost, and trends for improving product reliability through corrective actions.
We want a model that explains our data well but doesn’t overfit or add unnecessary complexity. This is where AIC and BIC come in. These criteria help us balance accuracy with simplicity, guiding us to the model that best fits the data without over-complicating things.


AIC (Akaike Information Criterion)
Akaike Information Criterion (AIC) is a measure used to evaluate models by balancing fit and complexity.
AIC measures how well a model fits the data, while penalizing for complexity.

BIC (Bayesian Information Criterion)
Bayesian information criterion (BIC) or Schwarz information criterion (also SIC, SBC, SBIC) is a criterion for model selection among a finite set of models. 
BIC is similar to AIC but applies a stronger penalty for complexity, especially as sample size increases.

Generally models with lower AIC or BIC are generally preferred.

A set of candidate models was evaluated using multiple selection criteria, including log-likelihood, Akaike Information Criterion (AIC), Bayesian Information Criterion (BIC), and error-based metrics such as SSE. Among all models, DW3 (F) and GM (F) emerged as the top two based on their superior performance.
After analyzing the Model Comparison tables from C-SFRAT, we determined that the Discrete Weibull Type 3 model, with covariate F is the best model, with AIC of 122.199 and BIC of 127.935. The second best is the Geometric Model with covariate F with AIC of 125.323 and BIC of 129.625.

## Model Comparison (selecting top two models)
![](./media/Top_model.png)


Based on the provided dataset (failure-dataset-a5.csv), the file contains 31 test intervals (T = 1 to 31).
Applying Sturges' Rule — k = 1 + log₂(n) — to the total number of failures (n = 31)
k = 1 + log₂(31) = 5.95 ≈ 6 intervals

Applying Sturges’ Rule to the number of test intervals (n = 31) yields approximately 6 intervals. However, due to the non-uniform distribution of failures and the presence of a mid-phase spike, 8 intervals were selected. This allows for better resolution of changes in failure intensity while still maintaining reasonable smoothing.


An effort interval of 20 for covariate F was selected based on the observed distribution of failures. A significant concentration of failures occurs at higher F values (≥ 20), indicating a transition to a higher failure intensity region. Using 20 efforts per interval therefore provides a meaningful grouping that captures this shift while maintaining stability in intensity estimation.

# Assessment Using Reliability Demonstration Chart 

## Plot for MTTFmin
![](./media/RDC_1.png)
## Plot for twice of MTTFmin
![](./media/RDC_2.png)
## Plot for half of MTTFmin
![](./media/RDC_3.png)

# Comparison of Results

# Discussion on Similarity and Differences of the Two Techniques

# How the team work/effort was divided and managed

# 

# Difficulties encountered, challenges overcome, and lessons learned

# Comments/feedback on the lab itself
