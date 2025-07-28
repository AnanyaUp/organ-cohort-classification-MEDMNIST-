# Organ Classifier – ResNet18 on MedMNIST with Gradio Deployment

This project builds a deep learning pipeline to classify grayscale medical scan images of **11 different human organs**. It uses a modified **ResNet18** model trained on the **MedMNIST v2 (OrganMNIST)** dataset. The model is evaluated using both **organ-level** and **cohort-level classification**. For deployment, the project uses **Gradio**, making it accessible via a public web UI — all from Google Colab.

---

##  Live Demo

> Try the model now: [Gradio Live App](https://33b780528fc8d759ca.gradio.live)

---

## Features

-  Multi-class classification of 11 human organs
-  Cohort mapping (organs → central, limbs, urinary groups)
-  Custom multi-task model with dual-output heads
-  Performance evaluation with accuracy & confusion matrix
-  Deployed in **Colab** using **Gradio** (no external hosting required)

---

## Organs Covered

| Index | Organ         | Cohort            |
|-------|---------------|-------------------|
| 0     | Bladder       | Urinary Organs    |
| 1     | Femur-Left    | Limbs             |
| 2     | Femur-Right   | Limbs             |
| 3     | Heart         | Central Organs    |
| 4     | Kidney-Left   | Urinary Organs    |
| 5     | Kidney-Right  | Urinary Organs    |
| 6     | Liver         | Central Organs    |
| 7     | Lung-Left     | Central Organs    |
| 8     | Lung-Right    | Central Organs    |
| 9     | Pancreas      | Central Organs    |
| 10    | Spleen        | Central Organs    |

---

## Model Performance

| Task                  | Accuracy |
|-----------------------|----------|
| Organ Classification | ~92%     |
| Cohort Prediction     | ~95%     |

> Evaluation includes confusion matrices, classification reports, and accuracy plots.

---

## Dataset

- **Dataset:** OrganMNIST (from [MedMNIST v2](https://medmnist.com/))
- **Type:** Grayscale, 28x28 images, 11 classes
- **Source:** Public, lightweight medical dataset

---

## Architecture

- **Model:** Modified `ResNet18` (PyTorch)
- **Backbone:** ResNet18 with single-channel input
- **Dual-head:** One for organ classification, one for cohort classification
- **Loss:** CrossEntropy (multi-task, weighted)

---

## Gradio Web App

<p align="center">
  <img src="
