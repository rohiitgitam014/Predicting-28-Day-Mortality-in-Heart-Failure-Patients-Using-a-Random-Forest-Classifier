## Abstract

Heart failure is a common reason for hospitalization in the elderly and it is associated with significant mortality and morbidity. To facilitate epidemiological studies of heart failure, there is a need for high quality datasets to be made available to researchers. While several heart failure datasets have been established in Western countries, there is a paucity of data available from China. Understanding differences in patient populations and healthcare systems between China and other countries is important in providing optimal care. To help address this issue, we created a retrospective heart failure dataset using electronic health data collected from patients who were admitted to a hospital in Sichuan, China between 2016 and 2019. The dataset includes **168 variables** for **2,008 patients** with heart failure.

---

## Background

Heart failure is a common reason for hospitalization in the elderly and it is associated with significant mortality and morbidity. The disease affects over **6 million people** in the United States, with an estimated incidence of **21 per 1000 people** in the elderly.

Studies have reported that one-year mortality ranges from **20% to 60%** after hospitalization for acute heart failure, depending on comorbidities and co-existing medical conditions.

Many datasets have been developed to support studies on the epidemiology of hospitalized patients with heart failure. For instance, the Cleveland Heart Disease dataset contains **75 variables** in **303 patients** and it is widely used in clinical studies. Another widely used dataset is the Nationwide Inpatient Sample (NIS), a publicly available resource from the Healthcare Utilization Project (HCUP) that is supported by the Agency for Healthcare Research and Quality.

---

## Methods

Our study aimed to establish a heart failure database by extracting data from routinely collected electronic healthcare records. Data on subsequent hospital admissions and mortality were obtained at a mandatory follow-up visit at **28 days**, **3 months**, and **6 months** (if the patient was unable to reach the clinical centre, the follow-up visit was replaced by a telephone call).

The study was carried out retrospectively, selecting patients who had been admitted to **Zigong Fourth People's Hospital**, Sichuan, China, with heart failure between **December 2016 and June 2019**.

Informed consent was waived due to the retrospective design of the study.

The study complies with the Declaration of Helsinki and was approved by the ethics committee of Zigong Fourth People's Hospital (**Approval Number: 2020-010**).

Electronic healthcare records of consecutive patients diagnosed with heart failure were reviewed.

Heart failure was defined according to the **European Society of Cardiology (ESC)** criteria:

- Presence of symptoms and/or signs of heart failure
- Elevated BNP (>35 pg/mL) and/or NT-proBNP (>125 pg/mL)
- Objective evidence of structural or functional cardiac abnormalities
- Additional diagnostic testing when necessary

Typical symptoms include:

- Breathlessness
- Orthopnea
- Paroxysmal nocturnal dyspnea
- Reduced exercise tolerance
- Fatigue
- Tiredness
- Delayed recovery after exercise
- Ankle swelling

Typical signs include:

- Elevated jugular venous pressure
- Hepatojugular reflux
- Third heart sound (Gallop rhythm)
- Laterally displaced apical impulse

---

## Data Description

Baseline clinical characteristics were measured on the day of hospital admission.

### Patient Information

- Body Temperature
- Pulse Rate
- Respiration Rate
- Systolic Blood Pressure
- Diastolic Blood Pressure
- Mean Arterial Pressure
- Weight
- Height
- Body Mass Index (BMI)
- Type of Heart Failure
- New York Heart Association (NYHA) Cardiac Function
- Killip Grade
- Glasgow Coma Scale (GCS)

### Echocardiographic Findings

The dataset includes:

- Left Ventricular Ejection Fraction (LVEF)
- Left Ventricular End Diastolic Diameter
- Mitral Valve Peak E Wave Velocity
- Mitral Valve Peak A Wave Velocity
- E/A Ratio
- Tricuspid Valve Regurgitation Velocity
- Tricuspid Valve Regurgitation Pressure

### Medication Data

Medication information is stored in **dat_md.csv**.

Administration times are not available, but multiple entries indicate multiple administrations.

Primary drug categories include:

#### Diuretics

- Furosemide
- Torsemide
- Spironolactone

#### Inotropes

- Deslanoside
- Dobutamine
- Digoxin
- Isoprenaline
- Milrinone

#### Vasodilators

- Isosorbide Mononitrate
- Nitroglycerin

---

## Usage Notes

The dataset was collected with the objective of developing predictive models for **emergency readmission of discharged heart failure patients**.

Other potential applications include:

- Mortality prediction
- Clinical risk prediction
- Comparative studies across hospitals and countries
- Machine Learning and Deep Learning research
- Healthcare analytics

### Limitations

- Data collected from a single medical center.
- Models developed using this dataset may not generalize to other hospitals or populations.
- The dataset is aggregated into one row per hospitalization.
- No longitudinal or time-series information during hospitalization is available.
- Medication administration timestamps are not included.

---

## Release Notes

### Version 1.3

Additional medications relevant to heart failure management were added, including:

- Metoprolol Tartrate Injection
- Heparin Sodium Injection
- Warfarin Sodium Tablet
- Enoxaparin Sodium Injection
- Clopidogrel Hydrogen Sulphate Tablet
- Aspirin Enteric-Coated Tablet

---

## Ethics

The study was approved by the Ethics Committee of Zigong Fourth People's Hospital.

**Approval Number:** 2020-010

---

## Acknowledgements

Zhang Z, Cao L, Chen R, Zhao Y, Lv L, Xu Z, Xu P.

**Electronic healthcare records and external outcome data for hospitalized patients with heart failure.**

*Scientific Data.*

2021 Feb 5;8(1):46.

DOI: **10.1038/s41597-021-00835-9**

PMID: **33547290**

PMCID: **PMC7865067**
