DEVS Data Divergence - Track 2 Final Submission

Team Name: Code Chemistry

Team Leader: Navin Pradeepan P D



***Project Overview:***

This project presents a physics-informed Machine Learning pipeline for 15-minute steel plant energy forecasting. Instead of treating the facility as a pure time-series problem, our model incorporates electrical kinematics, Apparent Power vectors, and diurnal cyclic features to accurately forecast usage and prevent maximum demand surcharge penalties.



Our final architecture is a Stacking Ensemble (75% Gradient Boosting / 25% Random Forest) achieving an RMSE of 8.1699 kWh under strict chronological validation.





***Repository / Folder Contents:***

DEVS\_Track2\_Steel\_Energy\_Model.ipynb: The master Jupyter Notebook containing EDA, feature engineering, training pipelines, and the final inference function.



elite\_ensemble\_system.pkl: Our final optimized and serialized Stacking Ensemble model.



train.csv: The dataset utilized for model training.



Steel Plant Energy Forecasting Executive Report.pdf: The comprehensive business and technical breakdown of our approach.



.png files: Supporting visualizations for feature importance, data drift, and performance comparisons.



***Instructions for Evaluators:***

To test this model against your hidden evaluation dataset, please follow these steps to ensure accurate and reproducible results:



Open DEVS\_Track2\_Steel\_Energy\_Model.ipynb in Google Colab or your local Jupyter environment.



Ensure both the hidden test dataset (e.g., test.csv) and elite\_ensemble\_system.pkl are uploaded to the active working directory.



Run the notebook to load the dependency libraries and the data preprocessing pipeline.



Scroll to the bottom of the notebook to the inference cell and pass your hidden test file into our automated pipeline:



predictions = run\_evaluation("test.csv")

print(predictions)



Note: Please evaluate exclusively using elite\_ensemble\_system.pkl. All intermediate models have been excluded from this directory to prevent versioning conflicts.

