# Nashville Housing Data Cleaning with SQL


## Executive Summary
This project focuses on the **critical process of data cleaning using SQL** on the **Nashville Housing Data** dataset.  
The goal was to transform a **raw, messy dataset** into a **clean, structured, and usable format** ready for in-depth analysis.  

Through a series of **SQL queries**, common data issues such as **missing values, inconsistent formats, and duplicates** were resolved to ensure **data integrity and reliability**.  
The final output is a **refined dataset** that can be used for **reporting and strategic decision-making** in the real estate market.

---

## Business Problem
In real-world data analysis, raw data is rarely clean.  
**Inaccurate or inconsistent data** can lead to **flawed insights** and poor business decisions.  

This project addresses the fundamental **business problem of data quality**, demonstrating how to prepare a dataset for **reliable analysis**.  
The objective is to create a **clean foundation** from which stakeholders can derive **accurate market insights** such as property value trends and sales patterns.

---

## Methodology
1. **Data Inspection**  
   - Identified missing addresses, duplicates, and inconsistent data types.  

2. **Date Standardization**  
   - Converted `SaleDate` into a consistent format for time-based analysis.  

3. **Handling Missing Values**  
   - Used **self-joins** on `ParcelID` to populate missing `PropertyAddress` values.  

4. **Data Structuring**  
   - Split combined address fields (`PropertyAddress`, `OwnerAddress`) into **Street, City, State** using functions like `SUBSTRING`, `CHARINDEX`, and `PARSENAME`.  

5. **Data Standardization**  
   - Unified the `SoldAsVacant` column values (e.g., Y/N → Yes/No) with a **CASE statement**.  

6. **Duplicate Removal**  
   - Applied **CTEs** with `ROW_NUMBER()` to identify and remove duplicate rows.  

7. **Column Management**  
   - Dropped unnecessary columns to streamline the dataset.  

---

## Skills Demonstrated
- **SQL**: Advanced querying and transformation techniques.  
- **Data Cleaning**: Handling missing, inconsistent, and duplicate data.  
- **Database Management**: Structuring columns, tables, and data types.  
- **Problem-Solving**: Real-world data quality challenges.  

---

## Results
The cleaning process delivered a **fully transformed dataset**:  
- All `PropertyAddress` nulls populated.  
- Addresses neatly separated into **Street, City, State**.  
- `SoldAsVacant` standardized to only **Yes/No**.  
- Duplicate records eliminated.  
- Redundant columns removed for efficiency.  

The dataset is now **ready for analysis** and **business intelligence applications**.  

---

## Business Recommendations
With the clean dataset, businesses can now explore:  
- **Market Trend Analysis** → Property value and sales trends over time.  
- **Geospatial Analysis** → Map-based insights on property sales in high-growth areas.  
- **Predictive Modeling** → Use in ML models to forecast housing prices.  
- **Strategic Planning** → Guide investments, acquisitions, and pricing strategies.
