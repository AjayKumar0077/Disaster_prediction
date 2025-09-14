🌍 Disaster Risk Prediction using World Risk Index Data

This project leverages machine learning to predict the World Risk Index (WRI) for different regions across the globe. The World Risk Index is a crucial measure that reflects a region’s disaster risk, determined by its exposure, vulnerability, susceptibility, and coping capacities.

By analyzing these factors, this project aims to provide valuable insights into disaster preparedness and risk reduction.

📊 Dataset

File: World_risk_index__cleaned_data.csv

Description: Contains World Risk Index values and its contributing indicators for various regions over multiple years.

Features

Region

Exposure

Vulnerability

Susceptibility

Lack of Coping Capacities

Lack of Adaptive Capacities

Year

Categorical risk levels for selected indicators

Target Variable

WRI (World Risk Index)

🔄 Project Workflow

Data Loading

Load dataset using pandas.

Exploratory Data Analysis & Preprocessing

Checked for missing values (none found).

Applied OneHotEncoder for categorical features.

Scaled numerical features with StandardScaler.

Data Splitting

Training (80%) / Testing (20%).

Model Selection & Training

Initial model: RandomForestRegressor.

Model Evaluation

Metrics: Mean Squared Error (MSE), R² Score.

Model Optimization

Used GridSearchCV to fine-tune hyperparameters.

Final Evaluation

Compared initial vs optimized performance.

Visualized Actual vs Predicted values & Residuals.

Performed 5-fold Cross-Validation.

✅ Results
Initial Model

MSE: ~0.0277

R²: ~0.9757

Optimized Model

Best Hyperparameters:

{'max_depth': 20, 'min_samples_split': 2, 'n_estimators': 100}


MSE: ~0.0273

R²: ~0.9761

Cross-Validation

Mean MSE (5-fold): ~0.0069

Conclusion: Model explains 97%+ variance in WRI, making it highly robust and reliable.

🚀 How to Run
Requirements

Install dependencies:

pip install pandas scikit-learn matplotlib numpy

Steps
# Clone the repository
git clone https://github.com/AjayKumar0077/Disaster_prediction.git

# Navigate into the project
cd Disaster_prediction

# Ensure dataset is present
World_risk_index__cleaned_data.csv

# Open Jupyter Notebook
jupyter notebook AIML_Disaster_prediction_project.ipynb

📈 Visualizations

Actual vs Predicted WRI values

Residual plots for error analysis

Feature importance plots

🔮 Future Improvements

Experiment with deep learning models for better accuracy.

Integrate time-series forecasting for disaster risk trends.

Deploy model using Flask/Streamlit for interactive risk prediction.

🤝 Contributing

Pull requests are welcome! Feel free to fork the repo, raise issues, and contribute improvements.

📧 Contact

Developed by Ajay Kumar
🔗 GitHub: AjayKumar0077
