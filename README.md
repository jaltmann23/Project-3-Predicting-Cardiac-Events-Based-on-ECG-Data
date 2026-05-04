# Predicting Cardiac Events Based on ECG Data
DSC 101 Project 3 (Final)

**Names:** Joseph Altmann & Kate Meinke

**Date Last Edited:** 5/4/26

## Overview
Congestive heart failure is a serious cardiac condition that affects millions of people worldwide. Early detection of dangerous cardiac events through ECG analysis can be life-saving. This project builds a logistic regression model using features extracted from long-term ECG recordings to predict cardiac events in patients diagnosed with severe CHF (NYHA class 3–4).

## Dataset Overview
**Source:** https://www.physionet.org/content/chfdb/1.0.0/

**Description:**
- 15 subjects with severe congestive heart failure (11 men, 4 women; ages 22–71)
- Each recording is approximately 20 hours in duration
- Two ECG signals per subject, sampled at 250 Hz with 12-bit resolution
- Data subsampled to take the first recording of each minute
- Annotation files (.ecg) generated via automated detector

**Variables**
- **ecg1:** The first ecg (electrocardiogram) reading for each patient
- **ecg2:** The second ecg reading for each patient
- **Cardiac Event:** The event that happens during each ecg reading
  - Normal Beats (N)
  - Ventricular Ectopic Beats (V)
  - Premature Beats (S/r)

**Files:**
- **.dat** - raw ECG signal data
- **.hea** - header files with recording metadata
- **.ecg** - annotation files

**Citation:** Goldberger, A., Amaral, L., Glass, L., Hausdorff, J., Ivanov, P. C., Mark, R., ... & Stanley, H. E. (2000). PhysioBank, PhysioToolkit, and PhysioNet: Components of a new research resource for complex physiologic signals. Circulation [Online]. 101 (23), pp. e215–e220. RRID:SCR_007345.

## Logistic Regression Model

**Libraries used:**
- **wfdb, os, re** - loading and reading data
- **numpy, pandas** - data processing
- **matplotlib, seaborn** - data visualization
- **sklearn** - model training and evaluation

**Features (X):** ecg1 and ecg2

**Target (y):** Cardiac Events

## Results

**Accuracy:** 0.98

**Precision:** 0.95

**Recall:** 0.98

**F1 Score:** 0.96
