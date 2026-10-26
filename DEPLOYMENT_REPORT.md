# Deployment Report — Student Service Request Monitoring System

## Reused work
- Preserved the submitted `Midterm_Examanition.ipynb` in this package.
- Used its documented Decision Tree classifier, `ColumnTransformer`, one-hot encoding for categorical fields, `max_depth=4`, and `random_state=42`.
- Followed the assignment's submission-time feature policy and excluded post-event fields from prediction.

## Changes made
- Added Streamlit navigation for Home, Dataset, Data Analysis, Prediction, Dashboard, and System Design.
- Added CSV schema checks, missing-value/duplicate summaries, interactive Plotly charts, a cached saved model, one-record inference, model metrics, dashboard review queue, requirements, workflow diagram, and SAD documentation.
- Included synthetic demo data and five example predictions to allow local testing without the missing source CSV.

## Tests and verification
- The app and modules are packaged for local execution; Python syntax compilation is checked before release.
- The package includes five sample prediction records in `sample_data/five_sample_predictions.csv`.
- A live Streamlit browser test and cloud deployment have not been performed in this environment. After installing dependencies, test each page, valid/invalid CSVs, prediction form, and downloads. Capture actual screenshots of each page and five prediction outcomes for submission.

## Limitations
- The actual `student_service_requests.csv` referenced by the notebook was not among the uploaded files. Therefore the included model was trained on synthetic demonstration data and must not be represented as the original midterm-trained model.
- Metrics from the final report (84.50% accuracy, 78.20% precision, 71.40% recall, F1 0.7463) could not be reproduced without the original dataset.
- The app does not implement authentication, a production API, or persistent logging of staff decisions. These should be added before operational use.
- Model estimates can produce false positives and false negatives. Human review is required; predictions must not automatically deny student services.

## Reflection
The project translates the midterm classification workflow into a navigable decision-support prototype. Its key system-design principle is separating prediction from authorized human action. Reproducibility and validity depend on restoring the original dataset and confirming that the deployed model matches the midterm experiment.

## URLs
- GitHub repository: TO BE ADDED AFTER YOU CREATE/PUBLISH THE REPOSITORY
- Streamlit deployment: TO BE ADDED AFTER DEPLOYMENT
