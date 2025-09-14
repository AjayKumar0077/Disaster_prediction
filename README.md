Disaster Risk Prediction using World Risk Index Data
This project aims to predict the World Risk Index (WRI) for different regions using machine learning. The model is built and evaluated based on various factors contributing to disaster risk, such as exposure, vulnerability, susceptibility, and coping capacities.

Dataset
The model is trained on the World_risk_index__cleaned_data.csv dataset. This dataset contains the World Risk Index and its component indicators for various regions over several years.

Features:

Region

Exposure

Vulnerability

Susceptibility

Lack of Coping Capabilities

Lack of Adaptive Capacities

Year

Categorical risk levels for various indicators

Target Variable:

WRI (World Risk Index)

Project Workflow
The project follows a standard machine learning pipeline:

Data Loading: The dataset is loaded into a pandas DataFrame.

Exploratory Data Analysis & Preprocessing:

The data is checked for missing values (none were found).

Categorical features are one-hot encoded using OneHotEncoder.

Numerical features are scaled using StandardScaler.

Data Splitting: The preprocessed data is split into training (80%) and testing (20%) sets.

Model Selection & Training: A RandomForestRegressor is chosen as the initial model and trained on the training data.

Model Evaluation: The initial model's performance is evaluated on the test set using Mean Squared Error (MSE) and R-squared (R²) scores.

Model Optimization: GridSearchCV is used to find the optimal hyperparameters for the RandomForestRegressor to improve its performance.

Final Evaluation: The optimized model is evaluated on the test set, and its performance is analyzed through visualizations of actual vs. predicted values and residual plots. K-fold cross-validation is also performed to ensure the model's robustness.

Results
The machine learning model demonstrated high accuracy in predicting the World Risk Index.

Initial Model Performance:

Mean Squared Error (MSE): ~0.0277

R-squared (R²): ~0.9757

Optimized Model Performance:

Best Hyperparameters: {'max_depth': 20, 'min_samples_split': 2, 'n_estimators': 100}

Mean Squared Error (MSE): ~0.0273

R-squared (R²): ~0.9761

Cross-Validation: The 5-fold cross-validation resulted in a mean MSE of approximately 0.0069, indicating a robust and reliable model.

The high R-squared score suggests that the model can explain over 97% of the variance in the World Risk Index based on the given features.

How to Use
To run this project, you will need to have Python and the following libraries installed:

pandas

scikit-learn

matplotlib

numpy

Clone the repository:

git clone [https://github.com/AjayKumar0077/Disaster_prediction.git](https://github.com/AjayKumar0077/Disaster_prediction.git)

Navigate to the project directory:

cd Disaster_prediction

Ensure the dataset World_risk_index__cleaned_data.csv is in the same directory.

Open and run the AIML_Disaster_prediction_project.ipynb notebook in a Jupyter environment.
