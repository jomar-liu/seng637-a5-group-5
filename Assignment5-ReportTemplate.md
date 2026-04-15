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
