# 🛒 Advanced Sales Data Analysis (Google Colab Project)

This repository contains a complete **end-to-end data analysis project** performed using **Python, Pandas, NumPy, Seaborn, and Matplotlib** in Google Colab.  
The dataset used is **Advanced_Dirty_Sales_Dataset.csv**, which includes sales transactions across multiple regions, cities, products, and customers.

The goal of this project is to clean, transform, analyze, and visualize sales data using 80+ real-world tasks.

---

## 📂 Dataset Columns
- **OrderID**
- **CustomerID**
- **CustomerName**
- **Product**
- **Category**
- **Quantity**
- **Price**
- **OrderDate**
- **City**
- **Region**
- **Returned**
- **TotalAmount**

---

## 🚀 Tasks Performed
### **🔹 Data Loading & Basic Exploration**
- Loaded CSV file using `pandas.read_csv()`
- Displayed shape, head/tail, columns, and dtypes
- Checked unique products, customers, regions

### **🔹 Data Cleaning**
- Converted price columns to numeric
- Fixed inconsistent date formats using `pd.to_datetime(errors='coerce')`
- Filled missing values (City → “Unknown”)
- Removed duplicates using `drop_duplicates()`
- Corrected uppercase/lowercase formatting
- Created lookup tables for Customer and Product
- Normalized text columns (lowercase, strip, remove special chars)

### **🔹 Feature Engineering**
- Extracted `Year`, `Month`, `Weekday`
- Created `OrderMonth`, `YearMonth`
- Calculated `UnitTotal`, mismatch flag
- Added `DiscountPrice` (10% discount)
- Added 7-day rolling averages
- Cumulative revenue per region
- High-value order flag (> 5000)
- Suspicious order flag (Quantity > 10 & Price > 1000)
- Extracted first names

### **🔹 Filtering & Querying**
- Orders from a specific city
- Returned orders
- Weekend orders
- Q1 orders
- Filter products containing substring ('top')

### **🔹 GroupBy Analysis**
- Total sales by Region
- Quantity sold per Region
- Average price per Category
- Average order value per Customer
- Customer revenue ranking
- Top 3 most sold products
- Count unique customers

### **🔹 Pivot & Melt**
- Pivot table of Region × Category
- Unpivot using `melt()`

### **🔹 Time-Series Analysis**
- Monthly revenue trend using `.resample('M')`
- Peak month per Region
- Monthly return count vs total orders
- YoY revenue growth
- Cities with 3+ months continuous growth

### **🔹 Encodings**
- One-hot encoding of region
- Transform normalization of TotalAmount

### **🔹 Visualizations**
- Heatmap of Quantity by City × Product
- Monthly revenue line chart
- Region-wise comparisons

---

## 📈 Key Insights
- East region generated highest revenue
- Phones & Laptops are the top-selling products
- Several dates were invalid and required repairing
- Nearly all rows contained mismatches in TotalAmount vs Quantity × Price (dirty dataset)
- Revenue has strong seasonality (monthly pattern)
- Return rate varies strongly by product and region

---

## 📁 Files in This Repository
- `sales_analysis.ipynb` — Google Colab notebook with full code  
- `lookup.csv` — CustomerID & Name lookup table  
- `east_data.csv` — Extracted East-region dataset  
- `README.md` — You are here 😊

---

## 🧠 Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Google Colab  
- GitHub  

---

## 💡 How to Run This Notebook
1. Open Google Colab  
2. Upload the notebook or link to GitHub  
3. Mount Google Drive  
4. Run all cells

---

## 🤝 Contributing
Pull requests are welcome. Please create a new branch before contributing.

---

## 📬 Contact  
Created by **Karthik** — Data Analyst  
Feel free to reach out for improvements or suggestions!
