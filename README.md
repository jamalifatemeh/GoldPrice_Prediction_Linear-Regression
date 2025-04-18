# GoldPrice_Prediction_Linear-Regression

This project uses **Linear Regression** to predict gold's opening price based on historical intraday trading data. The analysis spans from **January 16, 2023, to September 18, 2023** and involves data cleaning, feature engineering, model training, and evaluation.

---

## 📁 Dataset Description

The dataset (`Gold_data.csv`) contains:

- `date`: Date of the record
- `time`: Time of the record
- `open`: Opening price
- `high`: Highest price
- `low`: Lowest price
- `close`: Closing price
- `volume`: Trade volume

---

## 🧹 Methodology

### 1. Data Cleaning
- Removed outliers based on IQR in the `open` price.
- Ensured consistency and handled missing/null values.

### 2. Feature Engineering
- Used a **sliding window** approach:
  - 45 previous values as features (X)
  - 46th value as label (Y)
- Split data into:
  - 70% Training Set
  - 30% Testing Set

### 3. Model Training
- Used **Linear Regression** from `scikit-learn`
- Trained on sequences of 45-hour windows

### 4. Evaluation
- Evaluated using **Mean Squared Error (MSE)**
- Final model achieved **MSE ≈ 5.6**

---

## 📊 Visualizations

The project includes:

- Time-series plots for all price types (`open`, `high`, `low`, `close`)
- Box plot to detect outliers
- Prediction vs Actual line plots (full & zoomed)
- Final 500 true values + 200 predicted appended

---

## 🚀 Installation & Usage

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/gold-price-prediction.git
cd gold-price-prediction
```

### 2. Install Requirements

```bash
pip install numpy pandas scikit-learn matplotlib
```

### 3. Run the Script

```bash
python predict_gold.py
```

---

## 📈 Results

- Sample prediction: Predicted opening price of **1153**
- Mean Squared Error: **5.6**
- Model captures general trends but may benefit from advanced techniques.

---

## 🔮 Future Improvements

- Use **LSTM**, **XGBoost**, or **Random Forest** for better accuracy
- Introduce **technical indicators** (e.g., RSI, MACD)
- Implement **hyperparameter tuning**

---

## 📂 File Structure

```
gold-price-prediction/
├── Gold_data.csv
├── predict_gold.py
├── README.md
└── assets/
    └── [optional charts]
```

---

## 📄 License

MIT License.

---

Made for finance & forecasting enthusiasts 📈✨
