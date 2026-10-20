# ImanFarisha114/cardiomegaly-screening-detection
Uncertainty-Aware Deep Learning for Cardiomegaly Screening in Chest X-ray Images

A screening support tool that helps doctors detect cardiomegaly on frontal chest x-rays.
It gives a calibrated confidence score, a heatmap and the cardiothoracic ratio (CTR) so they can know whether the result can be trust or not.

## Problem statement
Doctors and radiologist who read chest x-rays by judging heart size mainly by eye, so the results depends on the reader's experience and mild cardiomegaly can be missed. Existing deep learning models for chest x-rays often give overconfident predictions without showing why they made a decision or when they might be wrong. Many of these models are also tested only on the dataset they were trained on, so they may perform worse on images from other hospitals. This matters because cardiomegaly i as key sign of heart disease and a missed or wrongly trusted result can be delay treatment.

## Documents
- [Problem statement](docs/problem-statement.md)
- [Requirements](docs/requirements.md)
- [User stories](docs/user-stories.md)

## Status
Planning (CSC649, Week 4)

## Author
Nur Iman Farisha Binti Mohd Jaafar
