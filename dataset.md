## Data Description

### Features:

1. Protected attribute, X = race, (*common protected attributes: race, religion, national origin, gender, marital status, age, and socioeconomic status; depends on problem domain and their relevant laws and policies*)
2. Confounders, Z = gender, age
3. Other variables, Z1 = age of offender at first offense (age_first_offence), and all other vars
4. Mediators, W =  juvenile offense counts (juv_fel_count), prior offencse counts (priors_count), degree of charge ()
5. Potential Biased Outcome, Y = recidivism score (two_year_recid)
6. x0 = "Male", x1 = "Female" (*taking help from 'fairness' R library by Drago Plecko*)
