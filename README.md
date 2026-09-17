# 📊 Shopify Stock Data – Exploratory Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on historical Shopify stock market data.

The analysis uses Python libraries such as **Pandas** and **Matplotlib** to understand stock price movements, daily returns, trading volume, price ranges, and moving averages.

The dataset contains **2,469 records and 7 columns**, covering Shopify stock data from **May 2015 to March 2025**.

---

## 🎯 Objectives

The main objectives of this project are:

* To load and inspect Shopify stock market data.
* To understand the structure and characteristics of the dataset.
* To check and handle missing values.
* To convert and organize the date column.
* To calculate daily price changes and daily returns.
* To analyze stock price ranges and trading volume.
* To calculate statistical measures such as mean, variance, and standard deviation.
* To visualize stock price and trading trends.
* To analyze 20-day and 50-day moving averages.
* To understand the distribution of daily returns.

---

## 🗂️ Dataset

The dataset contains the following columns:

| Column      | Description                        |
| ----------- | ---------------------------------- |
| `date`      | Trading date                       |
| `open`      | Opening stock price                |
| `high`      | Highest stock price during the day |
| `low`       | Lowest stock price during the day  |
| `close`     | Closing stock price                |
| `adj_close` | Adjusted closing price             |
| `volume`    | Number of shares traded            |

The original dataset contains **2,469 rows and 7 columns**. No missing values were found in the initial dataset.

---

## 🛠️ Technologies Used

* **Python 3**
* **Pandas**
* **Matplotlib**
* **Jupyter Notebook / Google Colab**

---

## 🔍 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the CSV dataset using Pandas.
2. Inspected the first few records using `head()`.
3. Checked the dataset shape and information.
4. Checked for missing values.
5. Converted the `date` column into datetime format.
6. Sorted the data according to date.
7. Set `date` as the DataFrame index.
8. Removed any remaining missing values.

---

## 📈 Feature Engineering

Three additional features were created:

### 1. Daily Price Change

Calculates the difference between closing and opening prices.

```python
df["Daily_Price_Change"] = df["close"] - df["open"]
```

### 2. Daily Return %

Calculates the percentage change from opening price to closing price.

```python
df["Daily_Return_%"] = ((df["close"] - df["open"]) / df["open"]) * 100
```

### 3. Price Range

Calculates the difference between the day's highest and lowest prices.

```python
df["Price_Range"] = df["high"] - df["low"]
```

---

## 📊 Statistical Analysis

The project uses descriptive statistics to understand the dataset.

The following measures were calculated:

* Mean
* Variance
* Standard deviation
* Minimum
* Maximum
* Quartiles

The calculated **mean daily return is approximately 0.0864%**, while the **standard deviation is approximately 3.1198%**.

---

## 📉 Data Visualizations

The project includes the following visualizations:

### 1. Shopify Trading Volume Trend

A line chart is used to visualize changes in Shopify's trading volume over time.

### 2. Daily Return Distribution

A histogram is used to understand the distribution and frequency of daily returns.

### 3. Price Range Trend

A line chart shows the variation in the daily price range over time.

### 4. OHLC Price Chart

The project compares:

* Open price
* High price
* Low price
* Close price

over the available trading period.

### 5. Moving Average Analysis

The project calculates:

* **20-Day Moving Average**
* **50-Day Moving Average**

These are plotted together with the daily closing price to observe price trends.

```python
df["MA_20"] = df["close"].rolling(20).mean()
df["MA_50"] = df["close"].rolling(50).mean()
```

### 6. KDE of Daily Returns

A Kernel Density Estimation (KDE) plot is used to visualize the distribution of Shopify's daily returns.


## 📁 Project Structure

```text
EDA_Task_3/
│
├── EDA_Task_3.ipynb
├── SHOP_2015-05-21_2025-03-16.csv
└── README.md
```

---

## 🚀 How to Run the Project

### Step 1: Clone the repository

```bash
git clone <your-repository-url>
```

### Step 2: Open the notebook

Open:

```text
EDA_Task_3.ipynb
```

using **Jupyter Notebook** or **Google Colab**.

### Step 3: Install required libraries

```bash
pip install pandas matplotlib
```

### Step 4: Add the dataset

Place the Shopify CSV dataset in the appropriate project directory.

### Step 5: Run the notebook

Run the cells sequentially to perform the complete EDA.

---
<img width="1011" height="483" alt="Screenshot 2026-09-17 193748" src="https://github.com/user-attachments/assets/648052a6-366a-4e1e-a1cc-e59af307b298" />
<img width="496" height="278" alt="Screenshot 2026-09-17 193701" src="https://github.com/user-attachments/assets/3d8a1426-a691-4eae-9abd-73f9357c0b30" />
<img width="503" height="240" alt="Screenshot 2026-09-17 193443" src="https://github.com/user-attachments/assets/95428e5a-221c-41f2-a8e2-f61e690f6803" />

---
## 📌 Key Findings

* The dataset contains **2,469 trading records**.
* The dataset has **7 original columns**.
* No missing values were present in the original dataset.
* Shopify's stock prices show considerable variation across the analyzed period.
* Daily returns were calculated to study day-to-day price movements.
* Trading volume was analyzed using a time-series line plot.
* 20-day and 50-day moving averages were used to examine closing-price trends.
* Daily return distribution was analyzed using both a histogram and KDE plot.

---

## 📚 Conclusion

This project demonstrates the use of **Exploratory Data Analysis techniques on financial time-series data**.

Using Pandas and Matplotlib, the data was cleaned, transformed, statistically analyzed, and visualized. The analysis provides an understanding of Shopify's historical stock prices, trading volume, daily returns, price ranges, and moving-average trends.

This project is intended for **educational and analytical purposes** and does not provide investment advice.

