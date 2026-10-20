# Problem Statement

## Who is affected?
Users: radiologist, medical officers and general doctor who reads chest X-rays.
Stakeholders: patients who may have heart disease.
Organizations: hospitals and clinics, especially busy and under-staffed ones.

## What exactly is going wrong?
- Doctors judge heart size on chest X-rays mainly by eye, so results depend on the reader's experience, and mild cardiomegaly can be missed.
- Existing deep learning models often give overconfident predictions and do not show why they made a decision or when they might be wrong.
- Many models are tested only on the dataset they were trained on, so they may perform worse on images from other hospitals.

## Why does it matter?
- Cardiomegaly is a key sign of heart disease, so a missed case tend to delay the treatment.
- If doctors cannot tell when an AI results is unreliable, the may trust a wrong answer or ignore the correct answer.

## Evidence
- Lee et al. (2024): chest X-ray interpretation varies between readers, and mild cardiomegaly can be missed.
- Yanar et al. (2025): cardiomegaly is a key radiological indicator of cardiovascular conditions.
- Guo et al. (2017): modern neural networks are poorly calibrated, so their confidence does not match their accuracy.

## Problem statement (3 to 5 sentences)
[Combine your three answers above into one short paragraph.]

## Scope
**In scope:**
- Binary classification: cardiomegaly vs normal
- Frontal PA chest X-rays only
- NIH Chest X-ray dataset for training; VinDr-CXR for external testing
- Calibrated confidence score, Grad-CAM heatmap and CTR measurement
- A simple web interface

**Out of scope:**
- Other chest diseases
- Lateral X-ray views
- Making a final diagnosis (the system only supports screening)
- Real hospital deployment or connecting to hospital systems
