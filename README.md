# 📊 Trader Sentiment Analysis

## Overview
This project explores the relationship between **market sentiment** (Fear & Greed Index) and **trader performance** using two datasets:
1. **Historical Trader Data** — Trade execution details from Hyperliquid.
2. **Bitcoin Market Sentiment Data** — Daily Fear & Greed Index values and classifications.

The objective is to uncover patterns, correlations, and actionable insights that can guide smarter trading strategies.

---

## 📂 Dataset Description

### 1. `historical_data.csv`
Contains historical trade execution records.
- **Key Columns:**  
  `account`, `symbol`, `execution price`, `size`, `side`, `Timestamp IST`, `Closed PnL`, `leverage`, etc.

### 2. `fear_greed_index.csv`
Contains daily Fear & Greed Index data.
- **Key Columns:**  
  `date`, `value` (0–100 scale), `classification` (e.g., Fear, Greed, Neutral, Extreme Fear).

---

## ⚙️ Steps Performed

### **1. Data Loading & Cleaning**
- Imported both datasets using Pandas.
- Converted timestamps to proper `datetime` objects.
- Standardized date formats for merging.

### **2. Data Merging**
- Merged datasets on `date` so each trade has an associated sentiment classification and index value.

### **3. Feature Engineering**
- Extracted **hour of day** from trade timestamps.
- Created `Trade Result` flag (Win/Loss) based on `Closed PnL`.

### **4. Analysis**
- Average, total, and count of PnL per sentiment.
- Win rates for each sentiment classification.
- Correlation between Fear & Greed Index value and PnL.
- Time-of-day performance patterns.
- Trade size impact on results.

### **5. Visualization**
- **Bar Plot:** Average PnL by sentiment.
- **Scatter Plot:** Index value vs. Closed PnL.
- **Box Plot:** PnL distribution by sentiment.
- **Line Plot:** Hourly PnL trends by sentiment.

---

## 📈 Key Insights
- Certain sentiments (e.g., *Greed*) showed higher average PnL and win rates.
- Trade sizes often increased in certain sentiment phases, sometimes amplifying losses.
- Clear time-of-day performance patterns emerged for specific sentiment phases.
- The Fear & Greed Index value showed a measurable correlation with trading performance.

---

## 🚀 How to Run the Notebook

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/trader-sentiment-analysis.git
   cd trader-sentiment-analysis
2. Install dependencies:
   ```bash
    pip install -r requirements.txt
4. Run the Jupyter Notebook cell by cell
   
## 🛠️ Technologies Used
Python 3

Pandas — Data manipulation

Matplotlib / Seaborn — Visualization

Jupyter Notebook — Analysis environment

## 📜 License
This project is for academic purposes and is not intended as financial advice.

## ✍️ Author
Prerit Sidhu


For questions or suggestions, feel free to reach out.


