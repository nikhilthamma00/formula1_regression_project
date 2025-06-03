# 🏎️ Formula 1 Qualifying Performance Analysis

This project explores how **tire wear affects lap times in Formula 1 qualifying sessions**, and whether different teams experience this impact differently. The analysis uses Python, pandas, and statsmodels to clean, analyze, and model telemetry data from the 2024 F1 season.

## 📌 Objective

The main research question is:

> **Does the performance gap between teams change as tire wear increases during qualifying sessions?**

We test whether some constructors experience a sharper drop-off in lap time due to tire degradation than others.

---

## 📁 Project Structure

- `project_formula1.ipynb`: Cleaned and commented Jupyter Notebook with code and analysis
- `data/`: Folder where session-level lap data is stored (not included here for privacy)
- `README.md`: This file

---

## 🧪 Methods Used

- **Data Cleaning**: Removed incomplete laps, converted units, engineered features like `TyreLife_Log`
- **Exploratory Data Analysis (EDA)**: Visualized lap time trends by team, tire condition, and temperature
- **Regression Modeling**: Used interaction terms between tire wear and team to detect differences in performance drop-off
- **VIF Checks**: Verified predictors had no multicollinearity

---

## 📊 Key Insights

- **Fresh tires** improve lap time by ~11 seconds on average during qualifying.
- **Tire degradation slows all teams**, but some suffer more than others.
- **Teams like Williams and Kick Sauber** showed larger lap time losses as tires aged, while **Red Bull and Alpine** handled wear better.
- **Track temperature** had a slight performance benefit, aligning with expectations that warmer conditions improve grip.
- **No multicollinearity** detected; all predictors were statistically interpretable.

---

## 📉 Tools & Libraries

- Python (pandas, numpy, matplotlib, seaborn)
- `statsmodels` for OLS regression
- `sklearn` for preprocessing
- `fastf1` API (for original data scraping, not shown in repo)
- Jupyter Notebook

---

## 🔍 Future Improvements

- Add sector-level breakdown to see where time loss occurs
- Include more telemetry (engine mode, fuel, DRS usage)
- Separate analysis by qualifying session (Q1, Q2, Q3)
- Apply fixed effects or panel data techniques for richer modeling

---

## 🤝 Acknowledgements

Built as part of an econometrics and business analytics project using real-world motorsport data. Special thanks to the creators of the FastF1 library and the Formula 1 community for enabling open telemetry analysis.
