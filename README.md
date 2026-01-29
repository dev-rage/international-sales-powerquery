# International Apparel Sales Data - Power Query Transformation Project

## 📋 Project Overview

This repository showcases a comprehensive Power Query data cleaning and transformation project using real-world messy data. The project demonstrates advanced data cleaning techniques applied to the **Amazon International Apparel Sales Dataset**, containing 37,432 rows of transactional sales data with significant quality issues.

**Project Type:** Data Cleaning & Transformation  
**Team:** Team WiDa  
**Tools:** Power Query, Power BI, Excel

## 📁 Repository Structure

```
international-sales-powerquery/
│
├── README.md                              # Project documentation
├── LICENSE                                # MIT License
├── .gitignore                             # Git ignore file
│
├── data/                                  # Dataset files
│   ├─── international_sales_raw_data.csv           # Original dataset (37,432 rows)
│   └─── International_sales_cleaned_data.csv       # Cleaned dataset (12,536 rows)
│
├── report/                                # Documentation & Reports
│   ├── Team_WiDa_PowerQuery_Task_Week_3_Report.docx  # Project report (Word)
│   └── Presentation_slides.pptx                       # Project presentation
│
└── dashboard/                             # Power BI Dashboard
    └── international_sales_report_analysis.pbix       # Interactive dashboard
```

## 📊 About the Dataset

### Amazon International Apparel Sales Data

- **Rows:** 37,432 transactions
- **Columns:** 10 fields
- **Period:** 2021 sales data
- **Domain:** International apparel/fashion retail

**Key Fields:**

- DATE, CUSTOMER, STYLE, SKU, SIZE, PCS (Quantity), RATE (Price), GROSS AMT

## 🔧 Data Quality Issues

The original dataset was characterized as "dirty" with multiple issues:

### 1. Missing Values

- ~1,040 rows with completely missing transactional data
- 2,474 rows missing SKU values
- Systematic gaps in critical fields

### 2. Categorical Chaos (Size Column)

- Mixed formats: Alphabetical (XS, S, M, L, XL), Numeric (1-15), Outliers (600, 698, 1000)
- Special labels and truncated codes

### 3. Formatting Issues

- Trailing punctuation (e.g., "XS.", "J0130-SET-L.")
- SKU concatenation errors
- Leading/trailing whitespace
- Mixed case inconsistencies

### 4. Structural Problems

- Dataset split into multiple tables within one file
- Redundant columns
- Mixed date formats (MM/DD vs DD/MM)
- Data scattered across different row ranges

## 🛠️ Power Query Transformations

### Step-by-Step Process:

1. **Data Connection** - Connected to CSV in Power BI and opened Power Query Editor

2. **Table Separation** - Split original dataset into two tables:

   - Table 1: Rows 1-18,634 (primary sales)
   - Table 2: Rows 19,676-37,432 (secondary sales with shipping data)

3. **Data Type Corrections** - Forced proper data types (dates, numbers, text)

4. **Text Cleaning**

   - Standardized case (uppercase/lowercase)
   - Trimmed whitespace
   - Removed trailing punctuation

5. **Column Extraction** - Extracted Size from SKU column for Table 2

6. **Query Appending** - Combined both tables into single dataset

7. **Deduplication** - Removed duplicates using (DATE, CUSTOMER, SKU) as composite key

8. **Final Validation** - Filtered out incomplete/invalid records

### Result:

✅ **From 37,432 to 12,536 rows** (66.5% reduction)  
✅ Clean, standardized, analysis-ready dataset

## 📈 Power BI Analysis

Created interactive dashboard with:

- **Date Table** using DAX (Month, Year, Quarter columns)
- Revenue analysis by customer, product, and time
- Sales distribution by size
- Seasonal trend analysis
- Customer segmentation

## 🔍 Key Insights

### Customer Concentration

- **72.4%** of revenue from top 5% of customers
- Key accounts: MULBERRIES BOUTIQUE, REVATHY LOGANATHAN

### Product Performance (80/20 Rule)

- **168 styles** drive **81%** of total revenue
- Clear Pareto distribution in inventory

### Size Distribution

- **L (Large):** 24.3% of sales
- **XL (Extra Large):** 22.1% of sales
- **M (Medium):** 18.7% of sales
- **Combined:** 65%+ of total volume

### Seasonal Trends

- Peak sales in **June 2021** and **September 2021**
- Critical for inventory planning

## 💡 Business Recommendations

1. **Implement data validation** at source to prevent quality issues
2. **Focus inventory** on top 168 revenue-driving styles
3. **Optimize stock** toward L, XL, M sizes (65% of demand)
4. **Strengthen relationships** with top 5% customers
5. **Prepare for seasonal peaks** in June and September
6. **Establish data governance** policies

## 🚀 How to Explore This Project

### 1. View the Data

- **Raw:** `data/raw/international_sales_raw_data.csv`
- **Cleaned:** `data/cleaned/International_sales_cleaned_data.csv`

### 2. Read the Documentation

- **Full Report (PDF):** `report/Team_WiDa_PowerQuery_Task_Week_3_Report.pdf`
- **Word Format:** `report/Team_WiDa_PowerQuery_Task_Week_3_Report.docx`
- **Presentation:** `report/Presentation_slides.pptx`

### 3. Explore the Dashboard

- Open `dashboard/international_sales_report_analysis.pbix` in Power BI Desktop
- Interact with visualizations
- Review data model and DAX measures

## 💻 Tools Used

- **Power Query** - Data transformation
- **Power BI Desktop** - Analysis & visualization
- **Microsoft Excel** - Data validation
- **DAX** - Custom calculations

## 📚 Skills Demonstrated

**Power Query:**

- CSV data connection
- Table splitting & restructuring
- Data type conversions
- Text transformations
- Column extraction
- Query appending
- Duplicate removal
- Advanced filtering

**Power BI:**

- Date table creation
- Data modeling
- DAX measures
- Interactive dashboards
- Report design

**Data Analysis:**

- Data quality assessment
- Business insight extraction
- Statistical analysis
- Recommendation development

## 👥 Team WiDa Members

1. Bashir Aminat
2. Lateefah Abdur-Rahman
3. Hawwa Atta
4. Jimoh Abdur-Rahman
5. Damilare
6. Oluwajuwonlo Wojuade
7. Toyyib A. Olalekan

## 👤 Contact

**[Wojuade Oluwajuwonlo]**

- GitHub: [@dev-rage](https://github.com/dev-rage)
- LinkedIn: [Wojuade Oluwajuwonlo](https://www.linkedin.com/in/oluwajuwonlo-wojuade-b2188023a/)
- Email: wojuadejuwon@gmail.com

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Mentorship program for guidance and learning materials
- Team WiDa for collaboration
- Power Query community for best practices

---

**Status:** ✅ Completed  
**Date:** January 2026  
**Week 3 Deliverable** - Power Query Mentorship Task

> _This project demonstrates practical data cleaning skills using Power Query on real-world messy data, showcasing the ability to transform dirty datasets into clean, analysis-ready data._
