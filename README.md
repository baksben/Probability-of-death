# Probability-of-death
In this project, I have to predict the probability of death of a patient that is entering an ICU (Intensive Care Unit), using K-Nearest Neighbor models.
The dataset comes from MIMIC project (https://mimic.physionet.org/). MIMIC-III (Medical Information Mart for Intensive Care III) is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.

Each row of mimic_train.csv corresponds to one ICU stay (hadm_id+ icustay_id) of one patient (subject_id). Column HOSPITAL_EXPIRE_FLAG is the indicator of death (=1) as a result of the current hospital stay; this is the outcome to predict in our modelling exercise. The remaining columns correspond to vitals of each patient (when entering the ICU), plus some general characteristics (age, gender, etc.), and their explanation can be found at mimic_patient_metadata.csv.
# Main tasks are:
Explore the data.
Clean the data.
Create new variables to help with predicting.
Using mimic_train.csv file build a predictive model for HOSPITAL_EXPIRE_FLAG*.
