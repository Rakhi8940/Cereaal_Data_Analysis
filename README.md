<p align="center"> <img src="https://github.com/user-attachments/assets/f617928b-f700-4264-b1f2-3c9d0022bbe4" width="900" alt="Cereal Rating Analysis Banner" style="margin: 12px 0; border-radius: 18px;"> </p> <br>
🥣 Cereal Rating Analysis

Cereal Rating Analysis is a data analytics and statistical modeling project that explores nutritional data of cereals to uncover patterns affecting consumer ratings. Using Python, it performs data preprocessing, statistical testing, visualization, and predictive modeling.

🎯 Objective
Analyze nutritional factors influencing cereal ratings
Handle missing and noisy data effectively
Perform statistical tests (ANOVA, Chi-Square, Correlation)
Visualize relationships between nutrients and ratings
Build a predictive model for cereal rating
📊 Dataset Description
Feature	Description
name	Cereal name
mfr	Manufacturer (A, G, K, N, P, Q, R)
type	Hot or Cold cereal
calories	Calories per serving
protein	Protein (g)
fat	Fat (g)
sodium	Sodium (mg)
fiber	Dietary fiber (g)
carbo	Carbohydrates (g)
sugars	Sugars (g)
shelf	Shelf display (1–3)
potass	Potassium (mg)
vitamins	Vitamins (0, 25, 100)
weight	Weight per serving
cups	Cups per serving
rating	Health rating (0–100)
🛠️ Technologies Used
Python
NumPy – Numerical operations
Pandas – Data manipulation
Matplotlib – Visualization
Seaborn – Advanced visualization
SciPy – Statistical testing
Scikit-learn – Machine learning
🧑‍💻 Project Workflow
# Importing libraries
import numpy as np
import pandas as pd
from matplotlib import pyplot as plt
import seaborn as sns
from scipy import stats

# Reading dataset
df = pd.read_csv('cereal.csv')

# Preview dataset
df.head()
🧹 Data Preprocessing
🔹 Handling Missing Values
Missing values represented as -1
Replaced with mean of respective columns
df = df.replace(-1, np.nan)
df = df.fillna(df.mean(numeric_only=True))
🔹 Handling Outliers
Used IQR method
Replaced extreme values with median
df[column] = np.where(df[column] > upper_bound, q2, df[column])
📈 Key Analysis & Insights
📌 Best & Worst Cereals
⭐ Best Rated: All-Bran_with_Extra_Fiber
❌ Worst Rated: Cap'n Crunch
📌 Manufacturer Insights
Kelloggs produces highest calorie cereal
Most cereals are cold type
📌 Nutritional Relationships
Sugars vs Rating: Strong negative correlation (-0.77)
Protein vs Rating: Positive correlation
Fat vs Rating: Negative correlation
📌 Correlation Highlights
Sugars & Calories → Positive (0.57)
Sugars & Carbs → Negative (-0.50)
Calories & Fat → Positive (0.51)
📌 Statistical Tests

🔬 ANOVA Test

Calories vs Rating → Significant relationship
Manufacturer vs Rating → Significant relationship

🔬 Chi-Square Test

Shelf vs Calories → Dependent variables
📊 Visualizations
📦 Rating vs Cereal Type
<p align="center"> <img src="https://via.placeholder.com/350x300?text=Rating+vs+Cereal+Type" width="400"> </p>
🔥 Correlation Heatmap
<p align="center"> <img src="https://via.placeholder.com/350x300?text=Correlation+Heatmap" width="400"> </p>
📊 Pairplot Analysis
<p align="center"> <img src="https://via.placeholder.com/350x300?text=Pairplot+Analysis" width="400"> </p>
📉 Calories vs Rating Trend
<p align="center"> <img src="https://via.placeholder.com/350x300?text=Calories+vs+Rating" width="400"> </p>
📊 Shelf vs Calories Heatmap
<p align="center"> <img src="https://via.placeholder.com/350x300?text=Shelf+vs+Calories" width="400"> </p>
🤖 Machine Learning Model
🔹 Linear Regression Model

Features used:

Protein
Fat
Sugars
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(x_train, y_train)
model.score(x_test, y_test)
📌 Model Performance
✅ Accuracy (R² Score): 0.86
Indicates strong predictive capability
🔌 Example Use Cases
Predict cereal ratings based on nutrition
Identify healthy vs unhealthy cereals
Optimize food product formulation
Consumer behavior analysis
📁 Project Structure
Cereal-Rating-Analysis/
├── data/
│   ├── cereal.csv
├── notebooks/
│   ├── analysis.ipynb
├── scripts/
│   ├── analysis.py
├── visuals/
│   ├── plots.png
├── README.md
└── ...
🧠 Future Improvements
Add advanced ML models (Random Forest, XGBoost)
Build interactive dashboards (Streamlit / Tableau)
Perform clustering for cereal segmentation
Add nutritional recommendation system
👩‍💻 Author

Made with ❤️ by Rakhi Yadav

<p align="center"> <b>Turning breakfast data into smart insights 🥣📊✨</b> </p>
