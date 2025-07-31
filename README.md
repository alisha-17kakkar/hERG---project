# hERG---project
# Predictive Modeling of hERG Inhibition for Cardiac Safety Assessment

## Project Summary

This project develops a machine learning model to predict whether a small molecule will block the hERG potassium channel, a critical factor in drug-induced cardiac toxicity. Early identification of hERG blockers can significantly de-risk the drug discovery pipeline, saving time and resources. This model leverages chemical data from the ChEMBL database and uses the RDKit library to translate chemical structures into a machine-readable format for prediction.

## Key Skills & Technologies
- **Programming Language:** Python
- **Libraries:**
  - **Cheminformatics:** RDKit
  - **Data Manipulation & Analysis:** Pandas, NumPy
  - **Machine Learning:** Scikit-learn
  - **Data Visualization:** Matplotlib, Seaborn
- **Data Source:** ChEMBL Database via web client
- **Environment:** Google Colab

## Methodology

The project followed a standard data science workflow:

1.  **Data Acquisition:** Programmatically downloaded and cached over 14,000 bioactivity data points for the hERG target from the ChEMBL database.
2.  **Data Cleaning & Preprocessing:** Filtered data for IC50 values, handled missing data, and established a binary classification threshold (active/inactive) at 10,000 nM.
3.  **Feature Engineering:** Converted chemical SMILES strings into numerical Morgan fingerprints (2048 bits) using RDKit, creating a feature set for the model.
4.  **Model Training:** Trained a Random Forest Classifier on an 80/20 train/test split of the data.
5.  **Model Evaluation:** Assessed model performance on the unseen test set using accuracy, precision, recall, and a confusion matrix.

## Results

The trained model demonstrated strong predictive performance on the test set, achieving an **overall accuracy of 81.83%**.

- **Precision (Active Class):** 84%
- **Recall (Active Class):** 84%

## Conclusion

This project successfully demonstrates the creation of an end-to-end cheminformatics workflow for a critical drug safety problem. The resulting model is a useful tool for prioritizing compounds in the early stages of drug discovery.
