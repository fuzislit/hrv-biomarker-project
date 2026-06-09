# Biomarker Discovery & Synthetic HRV Data Generation

**Rutgers University | Mentor: Dr. Daneault**  
**Jan 2026 – May 2026**

## Overview
This project develops a machine learning algorithm that generates synthetic physiological data to identify biomarkers of disease progression in rare neurological disorders such as ALS, Huntington's Disease, and Muscular Dystrophy.

Due to the scarcity of rare disease data, we trained models exclusively on healthy patient data to establish a normative baseline. Any future unhealthy patient data fed into the model will produce prediction errors that can flag disease progression.

## How It Works
- Extracted RR interval data from ECG signals of healthy individuals
- Trained CNN and LSTM models to predict the next heartbeat interval using a sliding window of 50 RR intervals
- Used LOOCV and K-Fold cross-validation to reduce overfitting
- Generated synthetic HRV data that closely mirrors real patient patterns

## Results
| Model | Mean RMSE | Mean MAE |
|-------|-----------|----------|
| CNN   | 30.29 ms  | 18.54 ms |
| LSTM  | 137.82 ms | —        |

CNN outperformed LSTM with more consistent and stable predictions across patients.

## Dataset
**Normal Sinus Rhythm RR Interval Database (NSR2DB)**
- 54 long-term ECG recordings from healthy individuals
- ECG digitized at 128 Hz with manual beat annotation review

## Tech Stack
- **Language:** Python
- **ML Models:** CNN, LSTM
- **Libraries:** TensorFlow, Scikit-learn, NumPy, Pandas, SciPy, Matplotlib, Seaborn, FastDTW
- **Environment:** Google Colab, Amarel Supercomputer

## Team
Fuzail Ali, Pablo Moreno, Nancy Shehata, Zain Iqbal, Erick Cruz  
Mentor: Dr. Daneault

## Future Goals
- Acquire rare neurological disease datasets to test against healthy baseline models
- Reduce prediction error further using improved hardware and more training epochs
- Expand synthetic data generation to support ALS progression research
  ## Presentation
[View Full Project Presentation](https://docs.google.com/presentation/d/1haIG59cB0vUrt7I6qe6d7fju6CtYSFUgJ4dcut1tq5M/edit?slide=id.g395a832d03f_1_1459#slide=id.g395a832d03f_1_1459)
