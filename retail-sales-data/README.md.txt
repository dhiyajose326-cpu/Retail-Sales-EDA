# 📊 **Retail Sales Exploratory Data Analysis (EDA)**

This project performs an **exploratory data analysis (EDA)** on a retail sales dataset containing 1,000 transaction records.
The goal is to identify insights related to customers, products, and sales trends.

---

## 📁 **Dataset Summary**

**Rows:** 1,000
**Columns:** 9

| Column           | Description                   |
| ---------------- | ----------------------------- |
| Transaction ID   | Unique transaction number     |
| Date             | Transaction date              |
| Customer ID      | Unique customer identifier    |
| Gender           | Customer gender               |
| Age              | Customer age                  |
| Product Category | Category of purchased product |
| Quantity         | Units purchased               |
| Price per Unit   | Price per item                |
| Total Amount     | Final bill per transaction    |

### ✔ Data Quality Report

* **Missing values:** 0
* **Duplicate rows:** 0
* **Date column:** stored as text (converted to datetime in EDA)

---

## 🔍 **Key EDA Results**

### **1. Descriptive Statistics**

| Feature        | Mean          | Std Dev | Min | Max  |
| -------------- | ------------- | ------- | --- | ---- |
| Quantity       | **2.51**      | 1.13    | 1   | 4    |
| Price per Unit | **179.89**    | 189.68  | 25  | 500  |
| Total Amount   | **456.00**    | 559.99  | 25  | 2000 |
| Age            | **41.39 yrs** | 13.68   | 18  | 64   |

✔ Customers are mostly middle-aged (average ~41)
✔ Purchases typically involve **1–4 items**
✔ Product prices vary widely (₹25 to ₹500)
✔ Total bill values range from low-cost items to premium baskets (up to ₹2000)

---

## 👥 **Customer Insights**

### **Gender Distribution**

* Males & females were both active buyers (balanced distribution)

### **Age Distribution**

* Most customers fall between:

  * **29–53 years old (IQR)**
  * Youngest: 18
  * Oldest: 64

Age groups created during EDA highlight:

* **26–35** and **36–50** age groups make the highest purchases.

---

## 🛍 **Product Insights**

* Product categories show clear variation in revenue contribution.
* Some categories dominate sales (from bar plot).
* Quantity vs Price scatter suggests:

  * Higher-priced products are bought in **lower quantities**.
  * Cheaper categories sell more units.

---

## 📈 **Time Series Insights**

(If your dataset lacked real dates, synthetic/cleaned dates were used.)

* Daily sales trend shows natural fluctuations.
* Monthly aggregation indicates:

  * Clear differences in peak and low-selling months.
  * Useful for planning inventory & promotions.

---

## 📊 **Visualizations Included**

The notebook contains:

* Correlation heatmap
* Daily sales line plot
* Monthly aggregated trend
* Gender-wise sales bar chart
* Age distribution histogram
* Sales by age group
* Sales by product category
* Quantity vs Price scatterplot

These visuals help understand both customer behavior and product performance.

---

## 💡 **Business Insights & Recommendations**

### **1. Age-focused marketing**

* Since ages **26–50** are the strongest buyers, campaigns should target working professionals.

### **2. Category-level inventory planning**

* High-performing categories should receive priority stock.
* Underperforming categories may need promotions or bundling.

### **3. Pricing strategy**

* Since high-priced items are bought in lower quantities, offering:

  * EMI options
  * bundle discounts
    may boost sales.

### **4. Identify loyal customers**

* Frequent buyers (based on Customer ID frequency) can be targeted for:

  * loyalty points
  * exclusive offers

---

## 🛠 **Technologies Used**

* Python
* Jupyter Notebook
* pandas
* numpy
* matplotlib
* seaborn

---

## ▶️ **How to Run the Project**

Clone the repo:

```bash
git clone https://github.com/yourusername/Retail-Sales-EDA.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open:

```
notebooks/EDA.ipynb
```

---

## 📦 **Project Structure**

```
Retail-Sales-EDA/
│
├── dataset/
│   └── retail_sales.csv
│
├── notebooks/
│   └── EDA.ipynb
│
├── README.md
└── requirements.txt
```
