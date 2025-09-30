# ⚡ Energy Consumption Forecasting (Keras)

Time-based energy consumption regression using **Keras**.  
This project builds baseline **Sequential** and **Functional** models (with a simple skip connection),
and demonstrates feature engineering with time-derived variables (Hour, DayOfWeek, Holiday, sin/cos transforms).

---

## 🎥 Analysis Video
Watch the analysis walkthrough here:  
👉 https://drive.google.com/file/d/1JZOftK5Q1GtS8dNQGlkl75iOl1r3mQTS/view?usp=sharing

---

## 📊 Dataset

The dataset used in this project is an **Energy Consumption dataset** provided in **Parquet (`.parquet`)** format:  

👉 https://drive.google.com/file/d/15paolMz3mbswXbdSYK6bLMOIA45VAcj1/view?usp=sharing

### Key Columns
- `Hour` → hour of the day (0–23)
- `DayOfWeek` → day index (0=Monday, 6=Sunday)
- `Holiday` → binary indicator (holiday / not holiday)
- `LightingUsage` → lighting power usage
- `Occupancy` → number of people present
- `EnergyConsumption` → target variable (total energy consumed)

The dataset is structured for **time-based regression**, where engineered features like `Hour_sin`, `Hour_cos`, and `Month_cos` are also included during preprocessing.

---

## ✨ Highlights
- Tabular regression with **Keras** (Sequential & Functional)
- Time features: `Hour`, `DayOfWeek`, `Holiday`, `LightingUsage`, `Occupancy`,
  plus periodic transforms such as `Hour_sin`, `Hour_cos`, `Month_cos`
- (Optional) hyperparameter search with **Keras Tuner**
- Clean EDA → training → evaluation in one notebook

---

## 📂 Repository Layout
```
energy-consumption-forecasting-keras/
├─ notebook/
│ └─ EnergyConsumptionForecasting.ipynb
├─ README.md
├─ requirements.txt
├─ LICENSE
└─ .gitignore
```

---

## 🛠 Environment
Install dependencies:
```bash
pip install -r requirements.txt
```
If you plan to run Keras Tuner, keep the keras-tuner dependency in requirements.txt.

---

## 🚀 Run the Notebook
```
jupyter notebook notebook/EnergyConsumptionForecasting.ipynb
```



