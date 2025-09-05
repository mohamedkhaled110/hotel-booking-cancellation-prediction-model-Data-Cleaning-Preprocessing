# Hotel Bookings Data Cleaning Project

## Overview
This project focuses on cleaning the **Hotel Bookings dataset** using Python (Pandas, Seaborn, Matplotlib).  
The dataset contains information about hotel reservations, cancellations, guest details, and booking information.  

The main objective was to:
1. Explore the dataset (EDA).
2. Identify and handle missing values, duplicates, and outliers.
3. Remove invalid or leakage columns.
4. Save a cleaned version of the dataset.

---

## Repository Contents
- **hotel_bookings.csv** → Original dataset.  
- **hotel_bookings_cleaned.csv** → Final cleaned dataset after processing.  
- **hotel_bookings.ipynb** → Jupyter/Colab notebook with step-by-step cleaning and plots.  
- **README.md** → Project description (this file).

---

## Cleaning Steps
1. **Missing Values**
   - `company` → filled with `"None"` (too many missing values).  
   - `agent` → filled with `"Unknown"`.  
   - `country` → filled with `"Unknown"`.  
   - `children` → missing values filled with `0`.  

2. **Duplicates**
   - Duplicate rows detected and dropped.

3. **Outliers**
   - `adr` (average daily rate) negative values replaced with NaN.  
   - `adr` values above `1000` were capped at `1000`.  

4. **Invalid Rows**
   - Removed ~180 rows where `adults + children + babies = 0`.

5. **Leakage Columns**
   - Dropped `reservation_status` and `reservation_status_date` (these reveal the booking outcome).

---

## Exploratory Plots
- Distribution of cancellations (`is_canceled`).  
- ADR distribution after cleaning.  
- Total guests per booking.  
- Top 10 countries by number of bookings.  
- Lead time distribution (days between booking and arrival).  

---

## How to Run
1. Open the notebook in **Google Colab** or Jupyter.  
2. Upload `hotel_bookings.csv`.  
3. Run all cells step by step.  
4. A cleaned file `hotel_bookings_cleaned.csv` will be generated.  

---

## Tools Used
- Python 3  
- Pandas  
- Seaborn  
- Matplotlib  

---

## Author
Prepared by **[Your Name]** as part of a data cleaning assignment.
