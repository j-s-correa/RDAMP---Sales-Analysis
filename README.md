# ACE Superstore - Sales Analysis Project Report

## Data Cleaning & Preparation

1. **Uploaded CSV File & Saved as Excel**  
   Started by importing the raw dataset into Excel. Immediately saved it as `.xlsx` to enable advanced cleaning tools like PivotTables and formulas.

2. **Date Formatting Issues**  
   Detected that the Date column was in U.S. format (MM/DD/YYYY) and stored as text.  
   Converted it into the UK format (DD/MM/YYYY) and ensured the column was set to Date format.

3. **Incorrect Region Values & Alignment**  
   The Region column had mismatches, empty cells, and wrong assignments.  
   Used `VLOOKUP` from the Store Locations dataset (based on the Postal Code) to correctly align the Region1 field.  
   The Country column was also incomplete and needed to be filled in. This was resolved using the same `VLOOKUP` approach, pulling country data from the Store Locations dataset.

4. **Missing Categories**  
   Found several empty cells in the Category column. Since there was no info to assign the correct values, I filled them with `"Others"` for analytical consistency.  
   Shortcut used in Excel: `Ctrl + G → Special → Blanks → type ="Others" → Ctrl + Enter`.

5. **New Aggregated Columns Created**  
   Added calculated fields for further analysis:
   - Final Sales per Unit  
   - Total Sales (with discount)  
   - Total Sales (without discount)  
   - Final Cost per Unit  
   - Total Revenue  
   - Profit per Unit  
   - Margin (%)
     
6. **Grouped Category for Improved Visualisation**
Created a "Plain Category" column to consolidate granular categories into broader classes for improved dashboard readability.

- This grouping simplifies segmentation and enhances clarity in Pivot Tables and charts.
-![image](https://github.com/user-attachments/assets/8adbd4c3-ce98-442b-b024-45af37a266e4)
-![image](https://github.com/user-attachments/assets/64bc61d9-147c-4b2e-835e-7b8a28002c64)
  
---

## Analysis & Visualizations

### 1. Total Sales, Revenue, and Discounts by Region  
Created a PivotTable to aggregate:
- Sales values with and without discounts  
- Revenue per region  

Identified performance by location and where margins were strongest or weakest.

---

### 2. Top 5 Best-Selling Products by Revenue  
Found via PivotTable sorted by Total Revenue.  
**Top products:**
- Portable Solar Generator  
- Portable Refrigerator Freezer  
- Electric Bike  
- Compact Dishwasher  
- Digital Camera  

These accounted for **£111,137.74** in revenue.

---

### 3. Bottom 5 Underperforming Products  
Identified the lowest revenue generators.  
Products like Cinnamon Raisin Bagels and Canned Black Beans generated revenue of under £5 each.

---

### 4. Highest Margins by Product Category  
Sorted average margin descending by category.  
**Top Categories by Margin% %:**
- Food - Dressing (78.7%)  
- Food - Salad Toppings (71.13%)  
- Food - Spices (69.97%)  
- Breakfast Foods and Cereals also ranked highly  

Useful for identifying where profit is best, even if sales volume is low.

---

### 5. Sales Channel Analysis: Online vs In-Store  
Created a PivotTable with the percentage of total sales and revenue:
- Online Sales: 51.50% of total, contributing £8.47M in revenue  
- In-Store Sales: 48.50%, contributing £7.96M  

Margins and profitability may differ even if sales volume is similar.

---

## Interactive Dashboard Logic

To make it more dynamic, I used the list option to create a drop-down parameter. Once the calculated field was created and linked to the parameter, I applied a filter where the condition returns “True” based on the selected dropdown value. Then, by dragging Country and Category into the view, we can display only the top revenue results.

---

## Final Presentation

Finally, I created a story using two dashboards, each presenting key insights, and combined them into a single, unified Tableau Story.

You can view the full interactive Tableau Public story here:  
[View Tableau Story on Tableau Public](https://public.tableau.com/app/profile/juan.correa./viz/RDAMP-AceSuperstore/AceSuperstoreInsights#1)

---

## Tools Used

- Excel: For data cleaning, VLOOKUP correction, pivot analysis, and formula-based feature creation  
- Tableau: For dynamic visualisation, interactive dashboards, and storytelling  
- Python: Considered for automation or advanced ETL steps in future phases

---

## Files Included

- Cleaned Excel dataset with calculated fields  
- Tableau workbook (.twbx)  
- Screenshots of key dashboards and visualisations  
- Link to Tableau Public Storyboard  

## 🔗 Project Files & Resources

 - 📂 [Juan_Correa Ace Superstore.xlsx](https://github.com/user-attachments/files/21105687/Juan_Correa.Ace.Superstore.xlsx)
 - 📄 [Juan_Correa_Sales_Report.docx](https://github.com/user-attachments/files/21105689/Juan_Correa_Sales_Report.docx)
 - 🌐 [Explore the RDAMP Tableau Dashboard (Live)](https://public.tableau.com/app/profile/juan.correa./viz/RDAMP-AceSuperstore/AceSuperstoreInsights#1)


