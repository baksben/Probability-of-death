# Probability-of-death
In this project, I have to predict the probability of death of a patient that is entering an ICU (Intensive Care Unit), using K-Nearest Neighbor models and SVM.
The dataset comes from MIMIC project (https://mimic.physionet.org/). MIMIC-III (Medical Information Mart for Intensive Care III) is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.

Each row of mimic_train.csv corresponds to one ICU stay (hadm_id+ icustay_id) of one patient (subject_id). <br>
Column HOSPITAL_EXPIRE_FLAG is the indicator of death (=1) as a result of the current hospital stay; this is the outcome to predict in our modelling exercise. The remaining columns correspond to vitals of each patient (when entering the ICU), plus some general characteristics (age, gender, etc.), and their explanation can be found at mimic_patient_metadata.csv.
# Main tasks are:
Explore and understand the dataset.<br>
Manage missing data.<br>
Manage categorical features. E.g. create dummy variables for relevant categorical features, or build an ad hoc distance function.<br>
Build a prediction model. Try to improve it using methods to tackle class imbalance.<br>
Assess expected accuracy of previous models using cross-validation.<br>
Run the predictions on the mimic_test_death.csv test file, and report accuracy by submitting to Kaggle page. Follow same preparation steps (missing data, dummies, etc).<br>
