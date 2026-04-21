<p align="center"> <img src="https://github.com/user-attachments/assets/f617928b-f700-4264-b1f2-3c9d0022bbe4" width="900" alt="Cereal Rating Analysis Banner"> </p>

# 🥣 Cereal Rating Analysis

Cereal Rating Analysis is a data analytics and statistical modeling project that explores nutritional data of cereals to uncover patterns affecting consumer ratings. Using Python, it performs data preprocessing, statistical testing, visualization, and predictive modeling.

## 🎯 Objective
- Analyze nutritional factors influencing cereal ratings
- Handle missing and noisy data effectively
- Perform statistical tests (ANOVA, Chi-Square, Correlation)
- Visualize relationships between nutrients and ratings
- Build a predictive model for cereal rating

## 📊 Dataset Description
| Feature |	Description |
|---------|-------------|
|name |	Cereal name |
|mfr |	Manufacturer (A, G, K, N, P, Q, R) |
|type	| Hot or Cold cereal |
|calories	| Calories per serving |
|protein |	Protein (g) |
|fat |	Fat (g) |
|sodium	| Sodium (mg) |
|fiber |	Dietary fiber (g) |
|carbo |	Carbohydrates (g) |
|sugars |	Sugars (g) |
|shelf |	Shelf display (1–3) |
|potass |	Potassium (mg) |
|vitamins |	Vitamins (0, 25, 100) |
|weight	| Weight per serving | 
|cups	| Cups per serving |
|rating |	Health rating (0–100) |

🛠️ Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn

## 🧑‍💻 Project Workflow
```python
# Importing libraries
import numpy as np
import pandas as pd
from matplotlib import pyplot as plt
import seaborn as sns
from scipy import stats

# Reading Dataset 
df = pd.read_csv('cereal.csv')

# Preview Dataset
df.head()
```

## 📈 Key Insights
- Best cereal: All-Bran_with_Extra_Fiber
- Worst cereal: Cap'n Crunch
- High sugar → lower ratings
- Protein improves rating
- Kelloggs has highest calorie cereal

## 📊 Visualizations
### Rating vs Cereal Type
<p align="center"> <img alt="image" src="https://github.com/user-attachments/assets/4ca4e0b6-2930-40ca-ae60-252fdb64fbd3" width="400"> </p>

### Correlation Heatmap
<p align="center"> <img alt="image" src="https://github.com/user-attachments/assets/7bd96441-7e0f-454f-b82b-97b665f9cfca" width="400"> </p>

### Pairplot
<p align="center"> <img alt="image" src="https://github.com/user-attachments/assets/07d7d830-656a-4b80-9626-b177970c5578" width="400"> </p>

### Calories vs Rating
<p align="center"> <img alt="image" src="https://github.com/user-attachments/assets/5abd8d93-378e-4697-9a1c-135bae04493f" width="400"> </p>

## 🤖 Model

### Linear Regression using:
- Protein
- Fat
- Sugars

### Accuracy (R²): 0.86
```
📁 Project Structure
Cereal-Rating-Analysis/
├── data/
├── notebooks/
├── scripts/
├── visuals/
└── README.md
```

## 🧠 Future Improvements
- Add advanced ML models
- Build dashboard (Streamlit / Power BI)
- Add clustering
- Recommendation system

## 👩‍💻 Author

Rakhi Yadav
### Turning breakfast data into smart insights 🥣📊✨
