# ICU Patient Dataset for Death Classification

This repository contains a dataset extracted from Electronic Health Records (EHR) of ICU patients. It includes patient records with demographic information, clinical measurements, severity scores, laboratory test results, ventilator settings, urine output, and the final patient outcome. The dataset is intended for use in the development and benchmarking of machine learning models aimed at predicting patient outcomes, specifically the likelihood of in-hospital death.

## Dataset Overview

The dataset is divided into two CSV files:

1. **X_train_2025.csv**: This file contains 3,600 patient records with 120 features that capture various aspects of patient data, including demographics, clinical measurements, and treatment-related information. It includes both static and dynamic features recorded over time.
   
2. **y_train_2025.csv**: This file contains the target variable, indicating the in-hospital death status (binary: 0 = survived, 1 = deceased) for each corresponding patient record in the training set.

## Features

The dataset includes the following types of features:

### Demographic and Admission Information:
- **recordid**: Unique identifier for each patient record.
- **Age**: Patient’s age.
- **Gender**: Patient’s gender (0 for female, 1 for male, or vice versa).
- **Height**: Patient’s height in cm.
- **Weight**: Patient’s weight in kg.
- **CCU, CSRU, SICU**: Binary flags indicating the type of ICU unit where the patient was admitted (e.g., Coronary Care Unit, Cardiac Surgery Recovery Unit, Surgical Intensive Care Unit).

### Severity Scores:
- **SAPS-I**: Simplified Acute Physiology Score, a severity of disease classification.
- **SOFA**: Sequential Organ Failure Assessment score, used to track a patient’s status during the ICU stay.

### Vital Signs and Clinical Measurements:
For several physiological parameters, there are multiple time-point measures:
- **[Parameter]_first**: The first recorded value upon ICU admission.
- **[Parameter]_last**: The last recorded value before discharge or death.
- **[Parameter]_lowest**: The minimum value recorded during the ICU stay.
- **[Parameter]_highest**: The maximum value recorded during the ICU stay.
- **[Parameter]_median**: The median value calculated across the ICU stay.

These parameters include:
- **DiasABP**: Diastolic arterial blood pressure.
- **GCS**: Glasgow Coma Scale score.
- **Glucose**: Blood glucose levels.
- **HR**: Heart rate.
- **MAP**: Mean arterial pressure.
- **RespRate**: Respiratory rate.
- **SaO2**: Blood oxygen saturation.
- **SysABP**: Systolic arterial blood pressure.
- **Temp**: Body temperature.

### Laboratory Test Results:
- **ALP, ALT, AST**: Liver enzymes.
- **Albumin**: Protein level in the blood.
- **BUN**: Blood urea nitrogen, kidney function indicator.
- **Bilirubin**: Liver function indicator.
- **Cholesterol**: Cholesterol level.
- **Creatinine**: Kidney function marker.
- **FiO2**: Fraction of inspired oxygen.
- **HCO3**: Bicarbonate level.
- **HCT**: Hematocrit.
- **K**: Potassium.
- **Lactate**: Blood lactate level, indicative of tissue hypoperfusion.
- **Na**: Sodium.
- **PaCO2, PaO2**: Arterial blood gas measures (CO2 and O2 partial pressures).
- **Platelets**: Platelet count.
- **TroponinI, TroponinT**: Cardiac biomarkers.
- **WBC**: White blood cell count.
- **pH**: Blood pH level.

### Ventilator and Urine Output Data:
- **MechVentStartTime**: Timestamp when mechanical ventilation was initiated.
- **MechVentDuration**: Total duration of mechanical ventilation (in hours or minutes).
- **MechVentLast8Hour**: Indicator showing whether mechanical ventilation was used during the last eight hours.
- **UrineOutputSum**: Total urine output during the ICU stay.

### Target Variable:
- **In-hospital_death**: A binary indicator (0 = survival, 1 = death) representing the patient's outcome during the hospital stay.

## Use Cases

This dataset is designed for:
- Predictive modeling of in-hospital death using machine learning techniques.
- Benchmarking different classification algorithms (e.g., logistic regression, random forests, support vector machines, neural networks).
- Exploring correlations between clinical features and patient outcomes.
- Developing decision support systems for ICU clinicians.

## Dataset Access

You can access the dataset through the following files:
- [X_train_2025.csv](ICU%20Patient%20Outcome%20Prediction/Directory%20actions/x-train-2025.csv)
- [y_train_2025.csv](link-to-y-train-2025.csv)

Please make sure to respect patient privacy and use this dataset for academic or research purposes only. All patient identifiers are anonymized, and no personally identifiable information (PII) is included.

## License

This dataset is licensed under the CC BY-NC-SA 4.0. Please refer to the LICENSE file for more information on terms of use.

## Citation

If you use this dataset in your work, please cite it as follows:
https://www.kaggle.com/datasets/fdemoribajolin/death-classification-icu
