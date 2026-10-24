# ImanFarisha114/cardiomegaly-screening-detection
Uncertainty-Aware Deep Learning for Cardiomegaly Screening in Chest X-ray Images

A screening support tool that helps doctors detect cardiomegaly on frontal chest x-rays.
It gives a calibrated confidence score, a heatmap and the cardiothoracic ratio (CTR) so they can know whether the result can be trust or not.

## Problem statement
Cardiomegaly screening from chest X-rays can be challenging for healthcare professionals because interpretation can be subjective, and mild cases may be missed K.-H. Lee et al., 2024). Although automated cardiothoracic ratio (CTR) measurement and deep learning models can help with screening, but the results can be affected by conditions such as scoliosis and lung consolidation Kufel et al., 2024). In addition, high model accuracy does not necessarily mean that the predictions are reliable, as confidence calibration remains under explored in medical image classification (Sambyal et al., 2023), while saliency-based heatmaps may have limited sensitivity and robustness when explaining chest X-ray predictions (Zhang et al., 2024). Therefore, there is a need for a cardiomegaly screening system for frontal PA chest X-rays that compares CNN and Vision Transformer models under the same conditions, reports calibrated confidence with visual explanations, flags uncertain cases for review, and checks its predictions against a CTR baseline and on external data.

## Documents
- [Problem statement](docs/problem-statement.md)
- [Requirements](docs/requirements.md)
- [User stories](docs/user-stories.md)
- [Sprint log](docs/sprint-log.md)

## Project structure
```
.
|-- README.md
|-- LICENSE
|-- .gitignore
|-- docs/
|   |-- problem-statement.md
|   |-- requirements.md
|   |-- user-stories.md
|   |-- sprint-log.md
|-- src/
    |-- README.md      (code will go here)
```
## Roadmap
- [x] Problem statement written
- [x] Requirements numbered and linked to user stories
- [x] User stories have acceptance criteria
- [x] Specialized technology chosen and explained
- [ ] First prototype (later in the semester)

## Status
Completed (CSC649, Week 4)

## Author
Nur Iman Farisha Binti Mohd Jaafar
