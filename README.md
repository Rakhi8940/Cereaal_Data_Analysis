<p align="center"> <img src="https://github.com/user-attachments/assets/f617928b-f700-4264-b1f2-3c9d0022bbe4" width="900" alt="Cereal Rating Analysis Banner"> </p>
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
NumPy
Pandas
Matplotlib
Seaborn
SciPy
Scikit-learn
🧑‍💻 Project Workflow
import numpy as np
import pandas as pd
from matplotlib import pyplot as plt
import seaborn as sns
from scipy import stats

df = pd.read_csv('cereal.csv')
df.head()
🧹 Data Preprocessing
Handling Missing Values
Missing values represented as -1
Replaced with mean
df = df.replace(-1, np.nan)
df = df.fillna(df.mean(numeric_only=True))
Handling Outliers
Used IQR method
Replaced with median
df[column] = np.where(df[column] > upper_bound, q2, df[column])
📈 Key Insights
Best cereal: All-Bran_with_Extra_Fiber
Worst cereal: Cap'n Crunch
High sugar → lower ratings
Protein improves rating
Kelloggs has highest calorie cereal
📊 Visualizations
Rating vs Cereal Type
<p align="center"> <img src="https://via.placeholder.com/350x300?text=Rating+vs+Cereal+Type" width="400"> </p>
Correlation Heatmap
<p align="center"> <img src="https://via.placeholder.com/350x300?text=Heatmap" width="400"> </p>
Pairplot
<p align="center"> <img src="https://via.placeholder.com/350x300?text=Pairplot" width="400"> </p>
Calories vs Rating
<p align="center"> <img src="https://via.placeholder.com/350x300?text=Calories+vs+Rating" width="400"> </p>
🤖 Model

Linear Regression using:

Protein
Fat
Sugars
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(x_train, y_train)
model.score(x_test, y_test)

Accuracy (R²): 0.86

📁 Project Structure
Cereal-Rating-Analysis/
├── data/
├── notebooks/
├── scripts/
├── visuals/
└── README.md
🧠 Future Improvements
Add advanced ML models
Build dashboard (Streamlit / Power BI)
Add clustering
Recommendation system
👩‍💻 Author

Rakhi Yadav
Turning breakfast data into smart insights 🥣📊✨
