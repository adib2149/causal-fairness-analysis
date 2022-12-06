# Fairness & Bias: High-level Overview and Ideation

---

## Preset

Assume we have the COMPAS dataset, we have a juror (*aka. model / causal model*) who follows an internal logic (*aka. algorithm / causal mechanism*). 

Assume we also have an existing dataset, based on the actions of this juror (*aka. COMPAS dataset*) in predicting recidivism on a certain population.

## What is the question we are looking for?

In broad terms, we want to know, **whether there was racial bias in predicting recidivism.**

The **causal question**: Are we marking individuals released on parole with high risk of re-offending within 2 years (Y) due to their race (X)? If yes, how di we mitigate that?

---

## Two Primary Research Questions

1. **Bias** (*Bias Quantification*) Is there a bias in the combination of model & dataset? How do we measure/ quantify bias?
2. **Fairness**: (*Bias Mitigation*) What are the changes in the policy/treatment needed, to mitigate the estimated bias?

---

## Questions to Quantify Bias

1. **Observational Bias**: check if african-americans are given more recidivism scores than caucasians? (aka. $E(Y|X1) - E(Y|X0)$ )
2. **Conditional Bias**: check if african-americans are given more recidivism scores than caucasians, conditional on all other variables? (aka. $\sum_z E(Y|X1,Z) - \sum_z E(Y|X0,Z)$ )

---

## Data Description

### Features:

1. Protected attribute, X = race, (*common protected attributes: race, religion, national origin, gender, marital status, age, and socioeconomic status; depends on problem domain and their relevant laws and policies*)
2. Confounders, Z = gender, age
3. Other variables, Z1 = age of offender at first offense (age_first_offence), and all other vars
4. Mediators, W =  juvenile offense counts (juv_fel_count), prior offencse counts (priors_count), degree of charge ()
5. Potential Biased Outcome, Y = recidivism score (two_year_recid)
6. x0 = "Male", x1 = "Female" (*taking help from 'fairness' R library by Drago Plecko*)
