# Requirements

## Functional requirements (what the system must DO)
1. FR1: The system shall allow the user to upload a frontal chest X-ray image in PNG or JPEG format.
2. FR2: The system shall classify the uploaded image as “Cardiomegaly” or “Normal”.
3. FR3: The system shall display a calibrated confidence score for each prediction.
4. FR4: The system shall generate a Grad-CAM heatmap showing the image regions that influenced the prediction.
5. FR5: TThe system shall compute and display the cardiothoracic ratio (CTR) from heart and lung segmentation.
6. FR6: The system shall label a prediction “Uncertain-needs review” when its confidence is below a set threshold.

## Non-functional requirements (how the system must PERFORM)
1. NFR1: (Performance) The system shall return the prediction, heatmap and CTR within 10 seconds per image.
2. NFR2: (Reliability) The model shall achieve an AURAC of at least 0.85 on the internal test set.
3. NFR3: (Security and privacy) The system shall not store uploaded images after the user’s session ends.
4. NFR4: (Usability) A first-timer user shall be able to obtain a result in no more than 3 steps.
