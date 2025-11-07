

# Climate Change Analysis 🌍

## Overview
This project analyzes global temperature changes and CO2 emissions over time. The goal is to understand how CO2 emissions correlate with global warming using Python, Pandas, and Seaborn.

---

## Datasets
1. **GlobalTemperatures.csv**  
   - Contains historical global temperature data, including average temperature by year.
2. **co2_emission.csv**  
   - Contains CO2 emission data by year.

---

## Tools & Libraries
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Project Structure

Climate_Change_Analysis/
│
├── GlobalTemperatures.csv
├── co2_emission.csv
├── climate_analysis.ipynb
├── plots/ # Folder containing all charts
└── README.md


---

## Steps of Analysis

### 1. Load Data
```python
import pandas as pd

temp = pd.read_csv("GlobalTemperatures.csv")
co2 = pd.read_csv("co2_emission.csv")

2. Clean Data

temp.dropna(inplace=True)
co2.dropna(inplace=True)

3. Exploratory Data Analysis (EDA)

    Plotting global temperature trends:

import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(12,6))
sns.lineplot(data=temp, x="Year", y="AverageTemperature")
plt.title("Global Average Temperature Over Years")
plt.savefig("plots/temp_trend.png")
plt.show()

    Analyzing CO2 trends and correlation:

merged_data = pd.merge(temp, co2, on="Year")

plt.figure(figsize=(10,6))
sns.scatterplot(data=merged_data, x="CO2", y="AverageTemperature")
plt.title("CO2 Emissions vs Average Temperature")
plt.savefig("plots/co2_vs_temp.png")
plt.show()

correlation = merged_data["CO2"].corr(merged_data["AverageTemperature"])
print(f"Correlation between CO2 and Temperature: {correlation}")

Key Findings

    Global temperatures have been steadily increasing over the past decades.

    CO2 emissions show a strong positive correlation with global temperature rise.

    The analysis emphasizes the impact of human activities on climate change.

How to Run

    Clone this repository:

git clone https://github.com/YourUsername/Climate_Change_Analysis.git

    Navigate to the project folder:

cd Climate_Change_Analysis

    Install required libraries:

pip install pandas numpy matplotlib seaborn

    Open climate_analysis.ipynb in Jupyter Notebook and run step by step.

Future Improvements

    Predict future temperatures using Machine Learning.

    Regional climate analysis.

    Advanced visualizations and dashboards.

Author

mennatallah taha
Data Analyst | Python & Data Visualization Enthusiast
www.linkedin.com/in/mennatallah-taha-433288353

