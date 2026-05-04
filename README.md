# EE559 Epilepsy Project: Epileptic Seizure Detection

This repository contains the codebase and dataset for the EE559 Epileptic Seizure Detection project. The primary focus of this project is to design, implement, and optimize a custom machine learning model to accurately detect epileptic seizures from raw EEG signal data.

## Project Overview

Epileptic seizures are sudden surges of electrical activity in the brain. In this project, we analyze 1 second EEG recording snippets to determine whether a seizure is occurring. 

Instead of relying entirely on prebuilt machine learning libraries, a major component of this project is the implementation of a custom Kernel Support Vector Machine (SVM) from scratch. We utilize the Sequential Minimal Optimization (SMO) algorithm and perform extensive hyperparameter tuning using grid search to maximize the F1 score for our custom model.

## Dataset

We use the **Epileptic Seizure Recognition Dataset**.
* **Features:** Each sample contains 178 data points representing 1 second of EEG recording sampled at 178 Hz.
* **Target:** The target variable `y` ranges from 1 to 5. Class 1 indicates seizure activity, while classes 2 through 5 indicate non seizure states (such as eyes open, eyes closed, or tumor area recordings). We formulate this as a binary classification problem: Seizure (Class 1) versus Non Seizure (Classes 2 to 5).

## Repository Structure

* **`EE559_Epilepsy.ipynb`**: The primary Jupyter Notebook. This file contains the data preprocessing, Principal Component Analysis (PCA) for dimensionality reduction, and the full implementation of our custom Kernel SVM with the SMO algorithm.
* **`EE559_Epileptic_Seizure_Baseline.ipynb`**: A supplementary notebook that establishes a baseline performance using standard library models to compare against our custom SVM implementation.
* **`Epileptic_Seizure_Recognition.csv`**: The EEG dataset used for training, validating, and testing our models.

## How to Run the Project

1. Ensure you have Python installed along with Jupyter Notebook or JupyterLab.
2. Install the necessary data processing packages (such as `numpy`, `pandas`, and `matplotlib`). Note that `scikit-learn` is only used for data splitting and evaluation metrics.
3. Clone this repository to your local computer.
4. Open the Jupyter notebooks and run the cells sequentially to observe the data processing steps, the custom model training, and the final evaluation results.
