# IPL First Innings Score Prediction Using Machine Learning

**Project Overview:**

This project focuses on predicting the first innings total score of IPL (Indian Premier League) cricket matches using machine learning models. By analyzing historical IPL data from 2008 to 2017, we aim to build a robust predictive model that can assist teams and analysts in strategic decision-making during live matches.

**Problem Statement:**

The goal is to build a machine learning regression model that accurately predicts the final score of the first innings in an IPL match using various match-related factors such as:

1. Batting & bowling team
2. Venue
3. Overs played
4. Wickets lost
5. Runs in the last 5 overs
6. Striker and non-striker performance

**Files Included:**

1. Final_Code.ipynb – Complete implementation notebook with EDA, feature engineering, model building, evaluation, and test cases.

2. ipl_data.csv – Cleaned IPL dataset (2008–2017) used for training and testing the models.

**Dataset Details:**

The dataset contains ball-by-ball IPL match data with the following key columns:

- venue, bat_team, bowl_team, batsman, bowler
- runs, wickets, overs
- runs_last_5, wickets_last_5
- striker, non-striker
- total – Final score of first innings (target variable)

Total Rows: ~76,000
Total Features: 15

**Key Steps in the Project:**

1. Data Cleaning & Preprocessing
- Filtered relevant columns and innings
- Handled missing values and inconsistent team names

2. Feature Engineering
- Used Label Encoding and One-Hot Encoding for teams and venue
- Created engineered features like batting and bowling performance metrics

3. Model Building
Tried multiple regression models:

- Linear Regression
- Decision Tree
- Random Forest (⭐ Best model)
- Gradient Boosting
- Neural Networks (MLPRegressor)

4. Evaluation Metrics

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score

5. Model Performance Comparison

| Model                | R² Score | RMSE  |
|---------------------|----------|--------|
| Linear Regression   | 0.53     | 20.86  |
| Decision Tree       | 0.82     | 12.73  |
| **Random Forest**   | **0.90** | **9.52** |
| Gradient Boosting   | 0.58     | 19.66  |
| Neural Network (MLP)| 0.76     | 14.71  |

Random Forest Regressor was selected for its superior accuracy and generalization.

6. Test Case Results
The model was evaluated on early, mid, and late innings scenarios. In most cases, the predicted scores were close to the actual outcomes, proving its real-time prediction capability.

**How to Run the Project**

1. Clone the Repository

git clone https://github.com/your-username/IPL-Score-Prediction.git
cd IPL-Score-Prediction

2. Install required libraries (if needed)

pip install pandas scikit-learn matplotlib seaborn

3. Open and run the notebook:

jupyter notebook Final_Code.ipynb

4. The notebook includes:

- Data loading from ipl_data.csv
- Preprocessing and EDA
- Model training, evaluation, and predictions

Future Enhancements:

- Deploy as a real-time Flask web app
- Add live match input form
- Integrate second innings predictions
- Improve model with more recent data

Use Cases:

1. Assist coaching staff with dynamic score forecasting
2. Enhance cricket broadcasting analytics
3. Add value to fantasy league platforms and cricket betting markets

Contact:
For queries or suggestions, feel free to reach out to me on Linkedin









