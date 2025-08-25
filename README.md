# Automated Sales Report (SQL Server)

## Table of Contents
1. [Project Inspiration](#project-inspiration)  
2. [Project Context](#project-context)  
3. [Project Goal](#project-goal)  
4. [Quantified Results](#quantified-results)  
5. [How It Helps Stakeholders](#how-it-helps-stakeholders)  
6. [Project Usage](#project-usage)  
7. [Download SQL File & Dataset](#download-sql-file--dataset)  
8. [Future Improvements](#future-improvements)  
9. [Project Takeaways](#project-takeaways)  

---

## Project Inspiration
I noticed many organizations still rely on manual Excel work to prepare sales reports. This often takes hours every week. To solve this, I created an **automated SQL Server procedure** that instantly generates daily, weekly, or monthly sales reports with just one command.  

---

## Project Context
The project uses a **Retail Superstore dataset** that contains:  
- 🛒 Sales transactions  
- 📦 Product information  
- 🏬 Store details  

This procedure automates reporting so that insights are delivered faster and more consistently.

---

## Project Goal
The project aims to:  
- ⏱️ **Save time** – reduce reporting from hours to seconds  
- ⚡ **Offer flexibility** – generate daily, weekly, or monthly summaries  
- 📊 **Provide insights** – breakdown by product, store, and region  

---

## Quantified Results
If deployed in a business environment, this project can achieve:  
- 📉 **60–70% reduction** in manual reporting time  
- ✅ More accurate and reliable reports  
- 🚀 Faster decision-making with real-time access to insights  

---

## How It Helps Stakeholders
- **Sales Managers** → Track sales by product and store daily/weekly/monthly  
- **Regional Managers** → Compare store performance across locations  
- **Executives** → Get monthly summaries for business growth tracking  
- **Finance & Operations Teams** → Access standardized and accurate data  

Reports can be embedded in **Power BI dashboards** or exported to Excel for sharing.

---

## Project Usage

### 1. Create the Stored Procedure
Run the SQL script in your SQL Server database.  
👉 See full script here: [`GetSalesReport.sql`](GetSalesReport.sql)

### 2. Generate Reports
Run the procedure with different parameters:

```sql
-- Daily Report
EXEC dbo.GetSalesReport @ReportType = 'Daily';

-- Weekly Report
EXEC dbo.GetSalesReport @ReportType = 'Weekly';

-- Monthly Report
EXEC dbo.GetSalesReport @ReportType = 'Monthly';

-- Example with filters
EXEC dbo.GetSalesReport 
    @ReportType = 'Monthly',
    @StoreID = 3,
    @ProductID = 101,
    @DateFrom = '2024-01-01',
    @DateTo = '2024-06-30';
```

---

## Download SQL File & Dataset
📂 [Download `GetSalesReport.sql`](./GetSalesReport.sql)  
📂 [Download Dataset](./RetailSuperstore_Dataset.csv)  

*(Upload both files in your GitHub repo root folder so these links work.)*

---

## Future Improvements
- ⬇️ Automatic export to Excel/CSV  
- ⏰ Schedule with SQL Agent  
- 📊 Direct integration with Power BI  
- 📆 Add YTD and QTD comparisons  

---

## Project Takeaways
This project proves how a simple SQL automation can:  
- Save **hours of manual reporting**  
- Provide **accurate and consistent insights**  
- Enable **faster business decisions**
