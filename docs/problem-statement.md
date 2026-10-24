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
- K.-H. Lee et al. (2024): visual interpretation of chest X-rays for cardiomegaly is subjective, and mild cases may be missed.
- Kufel et al. (2024): automated CTR measurement and deep learning results can be affected by conditions such as scoliosis and lung consolidation.
- Sambyal et al. (2023): confidence calibration remains under-explored in medical image classification, so high accuracy does not guarantee reliable confidence scores.
- Zhang et al. (2024): saliency-based heatmaps showed limited sensitivity and robustness when explaining chest X-ray predictions.
- Ahluwalia et al. (2023): four chest X-ray classifiers tested on 197,540 PA chest X-rays from a Canadian hospital network reached only 68% to 77% accuracy, with lower sensitivity for findings including cardiomegaly. This is the real example supporting the problem statement.

## Problem statement (3 to 5 sentences)
Doctors and radiologist who read chest x-rays by judging heart size mainly by eye, so the results depends on the reader's experience and mild cardiomegaly can be missed. Existing deep learning models for chest x-rays often give overconfident predictions without showing why they made a decision or when they might be wrong. Many of these models are also tested only on the dataset they were trained on, so they may perform worse on images from other hospitals. This matters because cardiomegaly i as key sign of heart disease and a missed or wrongly trusted result can be delay treatment.

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
