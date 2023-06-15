# Planning and Timeline

## High-level Overview
1. Pick a problem: define research question (is Y taking place due to discriminating treatment X, for population Z?)
2. Gather relevant dataset: COMPAS for now
3. Code to find answers to specific research questions
4. Explore all existing solutions
5. Find solutions to refute (internal or external validation)
6. Come up with varying approaches

## Two type of Pipeline
1. Generic ML Pipeline
2. Causal ML Pipeline

### Explore all these
https://expeditionhacks.com/nih-bias-detection-gallery/
https://github.com/adib2149/bias-detection-tools-challenge 

https://expeditionhacks.com/nih-bias-detection-gallery/
https://github.com/dplecko/CFA 
How about readme example


Build a very good example for causal fairness
Two questions: 
How to quantify bias 
\what's the policy recommendation for change in result
Steps:
Build a question
Answer causally
Parts:
Which use-case → data
Which model → method
Look at survey papers methods and data

Compile Focused Paper Set![image](https://github.com/adib2149/causal-fairness-analysis/assets/6183958/e5cc123c-13d1-4117-940c-30ec34bd9c6b)




Build a very good example for causal fairness
Focus NOT on “is there a bias (unfairness) available”, but on “is factor X causing the bias (is the machine unfair)”

Two questions: 
Q1: Bias Quantification and Prevalence (How to quantify bias)
Q2: Policy Adjustment for Bias Minimization (What's the policy recommendation for change in result)
Steps:
Build a question: Frame problem statement and SFM (X, Y, Z, W)
Answer causally: Find answers to Q1 & Q2
Parts:
Which use-case → data  Lets explore COMPAS dataset
Which model → method  Traditionally LR have been used, but we need to use causal tools
Look at survey papers methods and data



Explore Drago Plecko’s Code: 

Two directions on Causal FAIR: Lit review and our work on cosmos
— Using Elias's paper theory with an application / example to drive towards a policy
— Theoretical prospect: Start with Primer 4.4.4
Eventual move: Tutorial to Paper

Elias Paper Section 3 4 summary: Summary:
The framework is a direct child of SCM
We need the theory, we can formulate our problem using the theory
Ways to quantify the bias measures are ideated, but no exclusive example is given
No hands-on example with data or values are in the paper draft

