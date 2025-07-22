# 📌 Texas School Performance GAP Analysis

## 📖 Overview

This project analyzes academic performance across various independent school districts (ISDs) in the Houston,TX area using 2023-2024 STAAR data from the Texas Academic Performance Reports (TAPR). 

## 🎯 Aim
To uncover equity gaps among student groups and provide data driven insights into performance disparities by **Subject**, **Grade Level**, and **Demogrpahics**.

## 💾 Dataset Description

- **Source**: Texas Education Agency (TEA) - TAPR Reports
- **Files**: PDF reports from 6 Districts and a cleaned dataset
- **Size**: ~8250 Rows of student group performance data
- **Key Fields**:
  -   District Name, County, Grade, Subject
  -   Year (2023, 2024)
  -   Student Group (e.g, White, African American, Asian, Special Ed)
  -   Performace Category (Approaches, Meets, Masters)
  -   STAAR Performance Score Percentage

## 🧠 Analysis & Modeling Steps
  ### 🔹 Data Cleaning and Processing
  - Extracted tables from 2023-24 TAPR PDF reports using `pdfplumber`
  - Parsed district metadata (name, number, county) from file names
  - Mapped subjects and grade levels (e.g. "End of Course Algebra I" -> Grade 9)
  - Identified performance categories: Approaches, Meets and Masters
  - Processed demographic score rows for each subject and performance level
  - Merged cleaned outputs into a single dataset: `cleaned_data_final.csv`

  ---
  ### 🔹 Custom Power BI DAX Measures
  - **Average Score Metrics**
    - `Avg Score (2023)`, `Avg Score (2024)`, `Avg Score (All years)`
  - **Performance Level Measures**
    - `% Approaches`, `% Meets`, `% Masters`
  - **Equity and Comparison Measures**
       - `Gap From Top` , `Gap From Top Performing Group`, `Largest Equity Gap`
       - `Top Performing Group`, `Most Improved Group`, `Top Subject`
       - `State Avg Score (2024)`, `Top Group Score (2024)`
  ---
### 🔹 Visualization
  - Developed an interactive **Power BI dashboard** with above measures to explore trends and disparities:
    -  By **District**, **Grade Level**, **Subject**, and **Student Group**
    -  Includes slicers for filtering by **Year**, **Subject**, **Grade**, and **Performance Category**

## 📊 Key Findings
  - **Asian** students group leads performance in 2024 with an average STAAR score of **72.2%**
  - **Special Ed (Current)** students scored **43.5 points lower** than the top performing group in 2024.
  - Largest YoY Improvement: **American Indian Students**
  - Subject with highest underperformance: **Reading**, **Math**, and **Science**
  - District level performance shows **Clear Creek ISD** and **Cy-Fair ISD** outperform Houston ISD and Alief ISD
    
## 📷 Screenshots & Visuals
  Power BI dashboard screenshots and PDFs are available in ['/powerbi_visualizations'](./visualizations)
  - Executive Summary
  - STAAR Performance Review
  - Year Over Year Comparison
  - Equity Gap Analysis
  - Grade Level and Subject Detail
  - Comparison by District and County
  - Performance Category Breakdown
 
## 🚀 How to Run the Project
  1\. Open `notebooks/data_cleaning_and_processing.ipynb` to inspect the data pipeline <br>
  2\. Use  `cleaned_data_final.csv` for additional analysis or dashboard tools like Power BI <br>
  3\. Explore `/powerbi_visualizations` for pre-built insights and reporting PDF's

## 📚 Technologies Used
  - Python (`Pandas`, `Numpy`, `pdfplumber`)
  - Jupyter Notebooks 
  - Power BI (dashboard visuals)

## 🙌 Acknowledgements
  - Texas Education Agency (TEA) for providing TAPR data
  - Power BI community for visualization techniques
