# Biomarker Discovery & Synthetic HRV Data Generation

**Rutgers University | Mentor: Dr. Daneault**
**Jan 2026 – May 2026**

## Overview

🔗 **Project Website:** [View Project Overview & Results](https://fuzislit.github.io/hrv-biomarker-project/)

This research project explores machine learning approaches for generating synthetic heart rate variability (HRV) data and establishing healthy physiological baselines to support future research into rare neurological disorders, including ALS, Huntington's disease, and muscular dystrophy.

Using ECG-derived RR interval data from healthy individuals, we trained deep learning models to predict heartbeat intervals and evaluate how well they learned normal physiological patterns. The long-term goal is to investigate whether deviations from these baselines could help researchers identify potential indicators of disease progression.

## Data Processing & ETL

* Extracted RR interval data from ECG recordings of 54 healthy individuals.
* Processed physiological time-series data into sliding-window sequences of 50 consecutive RR intervals for model training.
* Prepared model inputs and training datasets using Python, NumPy, and Pandas.
* Developed a data preparation workflow to support model training, cross-validation, and performance evaluation.

## Machine Learning & Model Evaluation

* Developed CNN and LSTM models to predict the next RR interval from previous heartbeat measurements.
* Applied Leave-One-Out Cross-Validation (LOOCV) and K-Fold cross-validation to evaluate model performance across patient recordings.
* Evaluated prediction accuracy using Root Mean Squared Error (RMSE) and Mean Absolute Error (MAE).
* Generated synthetic HRV sequences to investigate how well the models reproduced patterns observed in healthy individuals.

## Results

| Model | Mean RMSE | Mean MAE |
| ----- | --------: | -------: |
| CNN   |  30.29 ms | 18.54 ms |
| LSTM  | 137.82 ms |        — |

The CNN achieved lower prediction error than the LSTM in the reported evaluation, demonstrating more accurate RR interval predictions on the evaluated data.

## Dataset

**Normal Sinus Rhythm RR Interval Database (NSR2DB)**

* 54 long-term ECG recordings from healthy individuals.
* ECG recordings digitized at 128 Hz with manual beat annotation review.

## Tech Stack

* **Language:** Python
* **Data Processing:** Pandas, NumPy, SciPy
* **Machine Learning:** TensorFlow, Scikit-learn
* **Models:** Convolutional Neural Networks (CNN), Long Short-Term Memory Networks (LSTM)
* **Visualization:** Matplotlib, Seaborn
* **Environment:** Google Colab, Amarel Supercomputer

## Team

**Project Manager:** Fuzail Ali
**Team Members:** Pablo Moreno, Nancy Shehata, Zain Iqbal, Erick Cruz
**Mentor:** Dr. Daneault

## Future Work

* Evaluate model performance using datasets containing rare neurological disease cases.
* Investigate whether prediction errors distinguish healthy physiological patterns from disease-associated patterns.
* Explore model improvements and additional synthetic data generation techniques.

## Presentation

[View Full Project Presentation](https://docs.google.com/presentation/d/1haIG59cB0vUrt7I6qe6d7fju6CtYSFUgJ4dcut1tq5M/edit?slide=id.g395a832d03f_1_1459#slide=id.g395a832d03f_1_1459)
