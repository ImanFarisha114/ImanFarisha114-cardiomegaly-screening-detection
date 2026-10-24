# Requirements

## Functional requirements (what the system must DO)
FR1: The system shall allow the user to upload a frontal chest X-ray image in PNG or JPEG format.
FR2: The system shall classify the uploaded image as “Cardiomegaly” or “Normal”.
FR3: The system shall display a calibrated confidence score for each prediction.
FR4: The system shall generate a Grad-CAM heatmap showing the image regions that influenced the prediction.
FR5: TThe system shall compute and display the cardiothoracic ratio (CTR) from heart and lung segmentation.
FR6: The system shall label a prediction “Uncertain-needs review” when its confidence is below a set threshold.

## Non-functional requirements (how the system must PERFORM)
NFR1: (Performance) The system shall return the prediction, heatmap and CTR within 10 seconds per image.
NFR2: (Reliability) The model shall achieve an AURAC of at least 0.85 on the internal test set.
NFR3: (Security and privacy) The system shall not store uploaded images after the user’s session ends.
NFR4: (Usability) A first-timer user shall be able to obtain a result in no more than 3 steps.