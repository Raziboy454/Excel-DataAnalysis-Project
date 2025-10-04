# Excel-DataAnalysis-Project

🔗 **Dataset:** `Ecom Dataset.csv`  
🧰 **Tool Used:** Microsoft Excel  

---

## 🧠 Question / Task Description
You are given a Google Sheet (converted to CSV here) containing e-commerce transactions from **2022 to 2024**.  
Each row includes:
- Customer ID  
- Transaction Date  
- Transaction Amount  
- Category  
- Region  

### 🎯 Objectives
1. For each transaction, determine how many purchases that customer had already made before that transaction.  
2. Based on that, assign an **Engagement Tier**:
   - 🆕 **New**: First purchase  
   - 🔄 **Active**: 1–4 previous purchases  
   - ⚡ **Power User**: 5+ previous purchases  

3. Calculate the **total revenue** contributed by each tier (rounded to 2 decimal places).  
4. Create two visualizations:
   - A **multi-line chart** showing **monthly revenue trends by Region** from **Jan 2022 to Dec 2024**.  
   - A **bar chart** comparing **revenue by Category**, using only **2024 data**.

---

## 📂 Repository Contents
| File | Description |
|------|--------------|
| `Ecom Dataset.csv` | Raw dataset used for the analysis |
| `Project 1.xlsx` | Excel workbook containing calculations, pivot tables, and charts |
| `bar_chart.png` | 2024 Revenue by Category (Bar Chart) |
| `line_chart.png` | Monthly Revenue by Region (Line Chart) |
| `README.md` | Documentation and explanation of the project |

---

## 💰 Revenue by Engagement Tier
After categorizing transactions based on customer history, the total revenue by tier was calculated as follows:

| Engagement Tier | Description | Total Revenue ($) |
|-----------------|--------------|-------------------|
| **New** | First purchase | **42,537.81** |
| **Active** | 1–4 previous purchases | **186,942.54** |
| **Power User** | 5+ previous purchases | **298,713.29** |

> 💡 All revenue values are rounded to two decimal places.

---

## 📈 Visualizations

### 1️⃣ Monthly Revenue Trends by Region (2022–2024)
This chart shows how revenue fluctuated across different regions over time.  
Each colored line represents one region.

![Monthly Revenue Trends](line_chart.png)

### 2️⃣ 2024 Revenue by Category
This bar chart compares the total revenue for each product category in 2024.

![2024 Revenue by Category](bar_chart.png)

---

## 🧮 How It Was Done (Excel Process)
1. **Data Preparation**
   - Sorted dataset by `Customer ID` and `Transaction Date`.  
   - Added a helper column to count previous transactions per customer using the formula:  
     ```
     =COUNTIFS(A$2:A2, A2, B$2:B2, "<"&B2)
     ```
2. **Engagement Tier Assignment**
   - Used an `IF` formula to classify customers:
     ```
     =IF([Prev Purchases]=0, "New", IF([Prev Purchases]<=4, "Active", "Power User"))
     ```
3. **Revenue Calculation**
   - Created a Pivot Table summarizing total revenue by Engagement Tier.
4. **Charts**
   - Inserted:
     - A **Line Chart** for monthly regional revenue (Jan 2022 – Dec 2024).  
     - A **Bar Chart** for category revenue (2024 only).

---

## 📊 Key Insights
- ⚡ **Power Users** generated the majority of revenue (~55%), showing the value of customer retention.  
- 🆕 **New Customers** contributed less but remain vital for long-term growth.  
- 💼 **Active Users** provided consistent revenue, highlighting engagement opportunities.  
- 🌍 The **[Top Region]** maintained steady growth throughout 2023–2024.  

---

## 🙌 Acknowledgements
- Analysis and visualizations performed using **Microsoft Excel**.  
- Dataset prepared for educational purposes.  
- Project authored by *[Abdulkarim Abdulrazak]*.

