# Planning and Timeline

## High-level Overview

The goal is to build a very good example / tutorial for causal fairness analysis. For bias estimation, the focus is not only on “is there bias (unfairness)”, but on “is factor X causing the bias”.

1. **Pick a problem**: define research question (is Y taking place due to discriminating treatment X, for population Z?)
2. **Gather relevant datasets**: A list of good benchmark datasets for causal fairness exploration
3. **Pick a dataset**: Starting with COMPAS dataset
4. **Pick a model/ pipeline**: Code to find answers to specific research questions
5. **Explore other relevant models/pipelines**: Explore varying approaches, to compare with the primary solution
6. **Refutation/ validation**: Find solutions to refute (internal or external validation)
7. **Writeup**: Create a slide/ paper draft to document all steps explored

## Task Distribution and Timeline

### Week 1-2: Get to know Causal Inference and Structural Theory of Causation
- [ ] Explore Primer Chapter 1, 2 (Background)
- [ ] Explore Primer Chapter 3 (do-calculus and adjustments)
- [ ] Explore Primer Chapter 4.4.4 (Unfairness)

### Week 3: Understand the Research Problem and Compile Relevant Papers
- [ ] Understand the research question of estimating (finding) & mitigating systemeatic bias/ unfairness, using causal inference tools
- [ ] Compile a set of research papers addressing this issue, organise in a Zotero folder and create a knowledge tree

### Week 4: Explore NCATS Bias Detection Challenge Tools and Bias Detection Tools
- [ ] Explore what has been recently done and gain an idea on the approach from [here](https://github.com/adib2149/bias-detection-tools-challenge) and [here](https://expeditionhacks.com/nih-bias-detection-gallery/)

### Week 5: 
- [ ] Explore Drago Plecko's code (Elias's Paper) from [here](https://github.com/dplecko/CFA)
- [ ] Explore the COMPAS dataset problem from their [README](https://github.com/dplecko/CFA#example)

## Two type of Pipeline
1. Generic ML Pipeline
2. Causal ML Pipeline

Two questions: 
Q1: Bias Quantification and Prevalence (How to quantify bias)
Q2: Policy Adjustment for Bias Minimization (What's the policy recommendation for change in result)
Steps:
Build a question: Frame problem statement and SFM (X, Y, Z, W)
Answer causally: Find answers to Q1 & Q2
Parts:
Which use-case → data  Lets explore COMPAS dataset
Which model → method  Traditionally LR have been used, but we need to use causal tools

## Two directions on Causal Fairness Analysis
— **Application perspective**: Using Elias's paper theory with an application / example to drive towards a policy
— **Theoretical perspective**: Start with Primer 4.4.4

## Summary from Elias's Paper on Causal Fairness (Section 3 & 4):
- The framework is a direct child of SCM
- We need the theory, we can formulate our problem using the theory
- Ways to quantify the bias measures are ideated, but no exclusive example is given
- No hands-on example with data or values are in the paper draft

