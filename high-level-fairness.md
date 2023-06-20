# Fairness & Bias: High-level Overview and Ideation

---

## Preset

Assume we have the COMPAS dataset, we have a juror (*aka. model / causal model*) who follows an internal logic (*aka. algorithm / causal mechanism*). We also assume the juror has a good understanding of the system and makes good predictions (*model with high performance*).

Assume we also have an existing dataset, based on the actions of this juror (*aka. COMPAS dataset*) in predicting recidivism on a certain population. Meaning this dataset has *predicted recidivism scores* and *actual recidivism scores*.

---

## What is the question we are looking for?

In broad terms, we want to know, **whether there was racial bias in predicting recidivism.**

The **causal question**: Are we marking individuals released on parole with high risk of re-offending within 2 years (Y) due to their race (X)? If yes, how di we mitigate that?

---

## Two Primary Research Questions

1. **Bias**: (*Bias Quantification*) Is there a bias in the combination of model & dataset? How do we measure/ quantify bias?
2. **Fairness**: (*Bias Mitigation*) What are the changes in the policy/treatment needed, to mitigate the estimated bias?

---

## Optimization Measure

Let's move forward with ***Total Variation (TV)***, as marked in "Causal Fairness Analysis" paper

---

## Questions to Quantify Bias - Pathway towards Bias

1. **(RQ1.1) Observational Bias**: 
    - estimate difference between predicted recidivism scores ( $Y_{pred}$ ) in between african-americans and caucasians
2. **(RQ1.2) Bias in Prediction**: 
    - estimate difference between predicted recidivism scores ( $Y_{pred}$ ) and actual recidivism scores ( $Y$ ) for african-americans and caucasians, check if there's differences
3. **(RQ1.3) Adjusted Bias in Prediction**: 
    - estimate difference between predicted recidivism scores ( $Y_{pred}$ ) and actual recidivism scores ( $Y$ ) for african-americans and caucasians (*same as above*), conditional on all other variables
4. **(RQ1.4) Bias in Model**:
    - estimate difference between new predictions of recidivism scores ( $Y_{pred}$ ), based on simulated and similar data but altered races
5. **(RQ1.5) Bias Detection libraries**: 
    - SolarIS, *check for others*
---
6. **(RQ1.6) Causal Bias with SCM**: 
    - given we known the **SCM** (along with known data & model), check if african-americans are given more recidivism scores than caucasians?
7. **(RQ1.7) Causal Bias with SFM**: 
    - given we known the **SFM** (along with known data & model), check if african-americans are given more recidivism scores than caucasians?
8. **Estimate Distribution of TV**: 


![width:300px](causal-effects-pathways.png)

---

## Questions to Mitigate Bias - Pathway towards Fairness

To my understanding, there is no **non-causal** version of this question. Because, if we can't identify which treatment variables to alter, there is no way of mitigating bias.

1. **(RQ2.1) Observational Fairness**: 
    - Explore feature importance / SHAP values / weights of features to see which factor has higher impact in decision making.
    - If only the variable race is changed in making predictions on model, would the model still have similar predicted recidivism scores?
2. **(RQ2.2) Causal Fairness by Policy Change**: 
    - What factors can be changed to minimize total variation (TV) between predicted recidivism scores of african-americans and caucassians?
3. **(RQ2.3) Causal Fairness by Unknown Race**:
    - If the variable race is not available in the dataset, would the model still have similar predicted recidivism scores?
4. **(RQ2.4) Causal Fairness by TV Breakdown**: 
    - How to remove direct and spurious effect but keep only indirect effect?
5. **Paper**: Explore all other definitions from paper 'Causal Fairness Analysis'
