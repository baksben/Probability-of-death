# Probability-of-death
In this project, I have to predict the probability of death of a patient that is entering an ICU (Intensive Care Unit), using K-Nearest Neighbor models and SVM.
The dataset comes from MIMIC project (https://mimic.physionet.org/). MIMIC-III (Medical Information Mart for Intensive Care III) is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.

Each row of mimic_train.csv corresponds to one ICU stay (hadm_id+ icustay_id) of one patient (subject_id). <br>
Column HOSPITAL_EXPIRE_FLAG is the indicator of death (=1) as a result of the current hospital stay; this is the outcome to predict in our modelling exercise. The remaining columns correspond to vitals of each patient (when entering the ICU), plus some general characteristics (age, gender, etc.), and their explanation can be found at mimic_patient_metadata.csv.
# Main tasks:
Explore and understand the dataset.<br>
Manage missing data.<br>
Manage categorical features. E.g. create dummy variables for relevant categorical features, or build an ad hoc distance function.<br>
Build a prediction model. Try to improve it using methods to tackle class imbalance.<br>
Assess expected accuracy of previous models using cross-validation.<br>
Run the predictions on the mimic_test_death.csv test file, and report accuracy by submitting to Kaggle page. Follow same preparation steps (missing data, dummies, etc).<br>
# Review 
## Extended grading

| Criteria | Weighting (%) | Score | Justification | Improvements  |
|----------|---------------|-------|---------------|---------------|
|Code runs | 5            |  5    |              |               |
|Data preparation |	15 | 15 | A few nice exploratory plots produced, good pre-processing of dates to engineer age and night time admission features. Nice use of summaries of death rates to incorporate comorbidity extra data. IterativeImputer used to impute missing data and the data was scaled in the correct manner using the pipeline
|kNN(s) have been used | 10 | 10 | with explicit arguments for number of neighbours, weights and metrics  | 
|Probability of death for each test patient is computed  | 5 | 5 | 
|Accuracy | 5 | 4 | > 0.85
|Hyperparameter optimization | 10 | 8 | Reasonable grid searches, would have been good to see investigation of more different values of the number of neighbours, how did you narrow down to 160-200?
|SVM(s) have been used | 10 | 10 | with explicit arguments for cost, kernel and hyperparameters | 
|Probability of death for each test patient is computed  | 5 | 5 | 
|Accuracy | 5 | 4 | > 0.85
|Hyperparameter optimization | 10 | 8 | Good experimentation with kernels, although the grids for the cost and the hyperparameter gamma are not very convincing. Your optimal gamma lies on the edge of the grid which suggests smaller values would have performance better
|Class Imbalance Managed | 5 | 5 | Excellent understanding of Random under sampler and SMOTE show and probabilities reweighted!
|Neat code with titles and comments | 5 | 5 | Really good explanation of methods and thinking behind decision showing good understanding 
|Improved methods from those discussed in class | 10 | 3 | Experimentation with SMOTE, consideration of several different kNN metrics

Score: 87
