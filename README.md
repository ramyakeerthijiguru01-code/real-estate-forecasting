# 🏠 Real Estate Market Forecasting

> Predicting 12-month home price trends across major US cities 
> using time-series forecasting models.

---

## 📌 Project Overview

A real estate investment firm wants to know:
**"Which cities will see the highest property price 
growth in the next 12 months?"**

This project builds a forecasting model that:
- Analyzes 25 years of historical home price data
- Predicts future prices for 5 major US cities
- Ranks markets by predicted growth percentage
- Helps investors make data-driven decisions

---

## 📊 Final Results

| Rank | City | Current Price | Predicted Price | Growth (12M) | Model Error |
|------|------|--------------|----------------|-------------|-------------|
| 🥇 1 | New York | $652,307 | $705,427 | +8.14% | 1.87% |
| 🥈 2 | Chicago | $249,152 | $264,794 | +6.28% | 1.12% |
| 🥉 3 | Los Angeles | $752,508 | $774,341 | +2.90% | 1.96% |
| 4 | Houston | $191,907 | $194,139 | +1.16% | 3.63% |
| 5 | Phoenix | $269,175 | $266,175 | -1.11% | 6.01% |

---

## 📈 Key Business Insights

1. **New York** shows the strongest predicted growth (+8.14%)
   — top market for short-term investment

2. **Chicago** is undervalued with strong growth (+6.28%)
   at a much lower price point than New York or LA

3. **Los Angeles** is the most expensive market ($752K)
   but growth is slowing down (+2.90%)

4. **Phoenix** shows a slight decline (-1.11%)
   — high risk market, avoid short-term investment

5. **All models achieved under 6% error (MAPE)**
   — reliable enough for strategic decisions

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Pandas | Data cleaning & manipulation |
| Prophet | Time-series forecasting model |
| Matplotlib | Data visualization |
| Scikit-learn | Model error metrics |
| VS Code | Development environment |

---

## 📁 Dataset

- **Source:** Zillow Research Data (zillow.com/research/data)
- **File:** City_Zhvi_AllHomes.csv
- **Size:** 27,330 cities × 300 months
- **Records:** 5.9 million rows after reshaping
- **Period:** January 1996 — March 2020

---

## 🔧 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/real-estate-forecasting.git
cd real-estate-forecasting
```

### 2. Install required libraries
```bash
pip install pandas numpy matplotlib prophet scikit-learn openpyxl
```

### 3. Download the dataset
- Go to: https://www.zillow.com/research/data/
- Download: **City_Zhvi_AllHomes**
- Place in the `Data/` folder

### 4. Run the notebook
```bash
# Open VS Code
code .
# Open forecasting.ipynb and run all cells
```

---

## 📂 Project Structure

RealEstate_Forecasting/
│
├── 📓 forecasting.ipynb       ← Main notebook
│
├── 📁 Data/
│   └── City_Zhvi_AllHomes.csv ← Raw dataset
│
├── 📁 Outputs/
│   ├── price_trends.png        ← EDA chart
│   ├── New York_forecast.png   ← City forecasts
│   ├── Los Angeles_forecast.png
│   ├── Houston_forecast.png
│   ├── Phoenix_forecast.png
│   ├── Chicago_forecast.png
│   └── market_rankings.csv     ← Final rankings
│
└── 📄 README.md

---

## 🔍 Methodology

### Step 1 — Data Collection
Downloaded Zillow's City-level Home Value Index (ZHVI)
covering 27,330 US cities from 1996 to 2020.

### Step 2 — Data Cleaning
- Reshaped data from wide format (300 columns) 
  to long format (3 columns)
- Removed missing values
- Filtered duplicate city entries by state

### Step 3 — Exploratory Data Analysis
- Plotted 25-year price trends for 5 major cities
- Identified 2008 housing crash impact per city
- Compared market recovery speeds

### Step 4 — Forecasting Model
- Used **Facebook Prophet** for time-series forecasting
- Trained on data up to 2019
- Tested on last 12 months of data
- Evaluated using **MAPE (Mean Absolute Percentage Error)**

### Step 5 — Market Ranking
- Calculated predicted 12-month growth % per city
- Ranked cities from highest to lowest growth
- Exported results to CSV

---

## 📉 Model Performance

| City | MAPE (Error%) | Rating |
|------|-------------|--------|
| Chicago | 1.12% | ⭐⭐⭐⭐⭐ Excellent |
| New York | 1.87% | ⭐⭐⭐⭐⭐ Excellent |
| Los Angeles | 1.96% | ⭐⭐⭐⭐⭐ Excellent |
| Houston | 3.63% | ⭐⭐⭐⭐ Good |
| Phoenix | 6.01% | ⭐⭐⭐ Fair |

> MAPE under 10% is considered good for real estate forecasting

---

## 🚀 Future Improvements

- [ ] Add more cities (Austin, Seattle, Miami)
- [ ] Include economic indicators 
      (interest rates, unemployment rate)
- [ ] Build interactive Streamlit dashboard
- [ ] Add rental price forecasting
- [ ] Try LSTM deep learning model

---

## 👩‍💻 Author

**Ramya Keerthi**  
Aspiring Data Scientist | Data Analytics Enthusiast  
📧 [your email]  
🔗 [your LinkedIn URL]

---

## 📜 License

This project is open source and available under 
the MIT License.