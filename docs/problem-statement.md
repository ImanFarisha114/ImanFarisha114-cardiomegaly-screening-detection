# Problem Statement

## Who is affected?
Users: radiologist, medical officers and general doctor who reads chest X-rays.
Stakeholders: patients who may have heart disease.
Organizations: hospitals and clinics, especially busy and under-staffed ones.

## What exactly is going wrong?
- Visual interpretation is subjective, and mild cases may be missed (K.-H. Lee et al., 2024).
- Automated CTR measurement and deep learning results can be affected by conditions such as scoliosis and lung consolidation (Kufel et al., 2024).
- High accuracy does not guarantee reliable predictions, as confidence calibration remains under-explored (Sambyal et al., 2023).
- Saliency heatmaps have limited sensitivity and robustness when explaining chest X-ray predictions (Zhang et al., 2024).
- Classifiers lose performance on new data, reaching only 68% to 77% accuracy on 197,540 PA chest X-rays from a Canadian hospital network, with lower sensitivity for cardiomegaly (Ahluwalia et al., 2023).

## Why does it matter?
- Missed mild cases causing some patients with an enlarged heart unreferred for further assessment (K.-H. Lee et al., 2024).
- Without calibrated confidence and reliable explanations, clinicians cannot tell when a model's prediction should be trusted, which limits its usefulness as a screening aid.

## Evidence
- K.-H. Lee et al. (2024): visual interpretation of chest X-rays for cardiomegaly is subjective, and mild cases may be missed.
- Kufel et al. (2024): automated CTR measurement and deep learning results can be affected by conditions such as scoliosis and lung consolidation.
- Sambyal et al. (2023): confidence calibration remains under-explored in medical image classification, so high accuracy does not guarantee reliable confidence scores.
- Zhang et al. (2024): saliency-based heatmaps showed limited sensitivity and robustness when explaining chest X-ray predictions.
- Ahluwalia et al. (2023): four chest X-ray classifiers tested on 197,540 PA chest X-rays from a Canadian hospital network reached only 68% to 77% accuracy, with lower sensitivity for findings including cardiomegaly. This is the real example supporting the problem statement.

## Problem statement (3 to 5 sentences)
Cardiomegaly screening from chest X-rays can be challenging for healthcare professionals because interpretation can be subjective, and mild cases can be missed, causing some patients with an enlarged heart unreffered for further assessment (K.-H. Lee et al., 2024). Although automated cardiothoracic ratio (CTR) measurement and deep learning models can help with screening, the results can be affected by conditions such as scoliosis and lung consolidation (Kufel et al., 2024). In addition, high model accuracy does not necessarily mean that the predictions are reliable, as confidence calibration remains under-explored in medical image classification (Sambyal et al., 2023), while saliency-based heatmaps may have limited sensitivity and robustness when explaining chest X-ray predictions (Zhang et al., 2024). For example, when four chest X-ray classifiers were tested on 197,540 posteroanterior (PA) chest X-rays from a Canadian hospital network, their accuracy fell to only 68% to 77%, with lower sensitivity for some findings, including cardiomegaly (Ahluwalia et al., 2023). Therefore, there is a need for a cardiomegaly screening system for frontal PA chest X-rays that compares CNN and Vision Transformer models under the same conditions, reports calibrated confidence with visual explanations, flags uncertain cases for review, and checks its predictions against a CTR baseline and on external data.treatment.

## Scope
**In scope:**
-	Binary classification of cardiomegaly vs normal (“No Finding”) chest X-rays
-	Frontal posteroanterior (PA) chest X-rays only
-	NIH Chest X-ray dataset for model training
-	Calibrated confidence score, Grad-CAM heatmap and automatically measured cardiothoracic ratio CTR
-	A simple web interface for uploading an image and viewing results


**Out of scope:**
-	Detection of other heart diseases and multi-label classification
-	Lateral chest X-ray views
-	Final diagnosis, as the system supports screening and does not replace qualified medical professionals
-	Real hospital deployment and integration with hospital systems, such as the Picture Archiving and Communication System (PACS)
