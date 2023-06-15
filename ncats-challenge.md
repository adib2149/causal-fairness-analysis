# NIH’s NCATS challenge: create a solution that detects bias in AI/ML models used in clinical decisions.

Submission deadline: **March 01, 2023**

## Some ideas to consider:

1.  How do you identify ***predictive*** and ***social*** bias?
2.  How do you account for “latent” bias where social or statistical biases happen over time due to the complexities of healthcare processes?
3.  Where does bias occur and how do we provide a path forward for follow-up investigations?
4.  How do you account for consistent evaluation and assessments of the algorithm over time and for all patient populations?

## Bias Types (defined by NCATS challenge)

1. **Predictive Bias**: Algorithmic inaccuracies in producing estimates that significantly differ from the underlying truth.
2. **Social Bias**: Systemic inequities in care delivery leading to suboptimal health outcomes for certain populations.

## Reason for inaccurate or unreliable AI/ML model/algo over time due to various factors; 

1. changes in data distribution
2. subtle shifts in the data
3. real world interactions
4. user behavior
5. shifts in data capture and management practices

## Steps to participate in challenge

1. Learn about the challenges of ***bias detection and mitigation*** through our upcoming educational webinars and engage with our mentors to explore how to ***identify*** and ***minimize*** harmful effects of AI/ML bias in healthcare.
2. Work with your team to come up with ideas. Check/seek help in Slack. 

## Target: be most successful at addressing all four items listed (Familiarize with challenge requirements and judging criteria):

1. Detect predictive and social biases
2. Identify source(s) of these biases
3. Prevent perpetuation of bias over time
4. Provide proof-of-concept as a tool that supports broad use of AI algorithms

---
## Submission Requirements

1. Github Repo (with two python scripts - .py files)
2. Max 3 submission (capturing only first 3)

1. “***measure_disparity.py***” takes in a set of model predictions and quantifies discrimination in model outcomes.
    - **Inputs**: A dataframe with one row per individual. Columns will include: 
        - Model prediction (as a probability)
        - Binary outcome (i.e. 0 or 1, where 1 indicates the favorable outcome for the individual being scored)
        - Model label
        - Sample weights
        - Demographic data on protected and reference classes
    - **Outputs**
        - One value per protected class measuring discrimination using the prescribed methodology
        - (*Optional*) graphics/visualization, useful formatted output

2. “***mitigate_disparity.py***” takes in a model development dataset (training and test datasets) that your algorithm has not seen before and generates a new, optimally fair/debiased model that can be used to make new predictions.

- **Inputs**: A model development dataset that contains information on:
    - Model features
    - Model label
    - Sample weights
    - Demographic data on protected and reference classes
- **Outputs**
    - The fair/debiased model object, taking the form of a sklearn-style python object with the following functions accessible:
        - .fit() – trains the model
        - .predict() / .predict_proba() – makes predictions using new data
        - .transform() – filters or modifies input data, if applicable
    - (*Optional*) graphics/visualization, useful formatted output

1. Python >= 3.8 
2. Must include “readme.txt” for installation instructions and “requirements.txt” for packages and versions. 
3. Submission through the docker image is optional, if necessary.

## Supporting documentation 

1. Code
2. Writeup
3. Video submission (*check rules later*)

PDF, max 10 pages. Use template provided and address these: 
1. Methodology Overview
2. Value Proposition
3. Healthcare Scenario
4. Operational Requirements
5. Sustainability Plan
6. Generalizability Plan
7. Implementation Requirements
8. Lessons Learned


## Judging Criteria

Determined by an evenly weighted average of scores from the judgement criteria listed below.

1. **Performance**:
    - Is the tool that has been developed accurate in identifying bias with the algorithm? What appropriate metrics are proposed to identify the bias?
        - Did they illustrate performance of the tool via retrospective (measuring performance of the clinical decision model when developed) and prospective (measuring performance continuity/in real world application) metrics?
    - Did the tool identify the type of bias inherent in the algorithm?  Is the bias predictive and/or social and how did the tool identify these biases?
        - Predictive Bias: algorithmic inaccuracies in producing estimates that significantly differ from the underlying truth.
        - Social Bias: systemic inequities in care delivery leading to suboptimal health outcomes for certain populations.
    - Do the implementation strategy and SOPs take into account or involve the multidisciplinary team and expertise needed for implementation in real-world settings?

2. **Feedback Loop**:
    - How well was the tool able to detect “latent” bias (i.e., increases in social or statistical biases over time due to the complexities of healthcare processes)?
    - Did the tool suggest follow-up investigations to identify the underlying root(s) of the biases detected?  How easily could the tool be implemented to perform this task?
    - Do these provisions seem adequate to ensure consistent evaluation and assessment of the algorithm over time and for all patient populations?

3. **Innovation**: 
    - How creative is this tool? Did it attempt to solve the problem with a novel approach?
    - If the tool creatively departs from existing practices and standards, how well-justified are those departures?
    - Does the tool seem likely to improve health equity (fairness) and trust in AI/ML in healthcare settings?

4. **Generalizability**:
    - How impactful is the tool? Who can use this tool and how likely are they to use it? How easily can the target user run it on an ongoing basis to monitor and continually improve bias mitigation practices?
    - Can this tool be deployed widely and if so, is an SOP and/or code etc. provided for implementation at other locations?
    - Are there any dependencies on vendors or proprietary information exchange standards that would limit its impact?
    - What are the next steps for this tool?  Can this tool be implemented as is or does it need additional support?

### The Evaluation Process.

A multidisciplinary Judging Panel composed of experts in related fields (e.g., clinical informatics, machine learning and artificial intelligence, bioinformatics, ethics) will evaluate all submissions against the judging criteria and submission requirements, including the outputs of the bias detection tool code against our healthcare models and data.

---
## Starter Kit Provided [(link)](https://docs.google.com/document/d/1wzZsMnl4UYE3du8XyMYNJT2xLNIAqN5c30vq5499fAI/edit#)

### Dataset:
1. Columbia Open Health Data (COHD)
2. SyntheticMass
3. Integrated Clinical and Environmental Exposure Data (ICEES)

### ML Algos:
1. Artificial Neural Networks (Conventional or Deep Learning), Logistic Regression, Random Forest, decision tree, and k-nearest neighbor
2. Bayesian models (such as Naive Bayes) and Gradient boosting (such as XGBoost)
3. Some example code and kaggle codes are also provided

---
## Bias Primer Provided [(link)](https://nihsncatsbias-gqi5483.slack.com/files/U0486HGKKB9/F04CR2PFNEL/bias_primer_from-solasai.pdf)

*Need to explore*

---
## FAQ

1. No ml model needed, just a general solution that will work with any ML model and data

