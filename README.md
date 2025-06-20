# ✈️ Airline Ticket Fare Prediction

This project focuses on predicting the fare of airline tickets using supervised machine learning techniques. It includes data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and evaluation.

## 📁 Project Structure

```
.
├── flight_prediction.ipynb  # Main notebook with all code
├── dataset/                 # Folder containing the dataset
├── plots/                   # Visualizations from EDA
└── README.md                # Project documentation
```

## 📌 Problem Statement

Airline ticket prices can vary significantly based on multiple factors. The goal is to build a machine learning model that predicts the price of a flight based on various features such as:

- Date of Journey
- Departure and Arrival Time
- Source and Destination
- Total Stops
- Airline
- Duration

## 📊 Dataset

The dataset used in this project was sourced from [https://drive.google.com/drive/folders/1QPizxIdGZ7TA9ecSGjDxJFLYNUOC8Kn9), and includes domestic flight information such as:

- `Airline`
- `Date_of_Journey`
- `Source`, `Destination`
- `Dep_Time`, `Arrival_Time`
- `Duration`, `Total_Stops`
- `Price` (target)

## 🔧 Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost (tested but not selected)

## 📈 Model Development

### Steps:
1. **Data Cleaning & Preprocessing**  
   - Handling missing values  
   - Feature engineering (extracting day, month, duration in minutes, etc.)  
   - Encoding categorical variables

2. **Exploratory Data Analysis (EDA)**  
   - Visualizing distribution of prices and relationships between features

3. **Model Building**  
   - Trained various models: Linear Regression, Random Forest, XGBoost  
   - Hyperparameter tuning with GridSearchCV

4. **Evaluation Metrics**  
   - R² Score  
   - Mean Absolute Error (MAE)  
   - Root Mean Squared Error (RMSE)

### Best Model:
- **RandomForestRegressor** performed best with an R² Score of **~0.86**

## ✅ Results

| Model            | R² Score | RMSE     |
|------------------|----------|----------|
| Linear Regression| 0.67     | 2500     |
| Random Forest    | 0.86     | 1800     |
| XGBoost          | **0.84** | **1900** |



## 🧪 How Was the Best Model Selected?

Choosing the right algorithm is a process of experimentation and tuning. Here's the approach used in this project:

### ✅ Model Selection Process

1. **Tried Multiple Algorithms**  
   - Linear Regression  
   - Random Forest  
   - XGBoost  

2. **Hyperparameter Optimization**  
   We used `RandomizedSearchCV` to find the best hyperparameters for Random Forest. This allows efficient searching through many combinations.

3. **Cross-Validation**  
   Applied 3-fold cross-validation to ensure the model generalizes well.

4. **Evaluated with Multiple Metrics**  
   - R² Score  
   - Root Mean Squared Error (RMSE)  
   - Mean Absolute Error (MAE)

5. **Considered Domain Knowledge**  
   Beyond metrics, we also considered which model makes more practical sense in real-world airline pricing scenarios.
   
## 📌 Future Improvements

- Use more recent datasets
- Deploy the model using Streamlit or Flask
- Implement cross-validation for more robust evaluation
- Add airline class (Economy, Business) as a feature

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/Emychisom/Predict-fare-of-Airlines-Tickets.git
   cd Predict-fare-of-Airlines-Tickets
   ```

2. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Open Jupyter Notebook:
   ```bash
   jupyter notebook flight_prediction.ipynb
   ```

## 🧠 Author

**Chisom Emy**  
📧 [LinkedIn](https://www.linkedin.com/in/chisom-mbah-974040319/)
