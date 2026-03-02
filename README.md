**📊 Sundry Debtors Analysis (2023–2025)
Project Overview**

This project analyzes Sundry Debtors data from three Excel files (**2023, 2024, and 2025**) using Python in Google Colab.

The objective is to:


Extract all debtor names under Sundry Debtors

Extract their individual amounts

Compare balances year-by-year

Classify payment behavior automatically

Identify new debtors appearing in later years

Export the final structured report to Excel


**Objectives**

The system performs the following:

Extract all debtor names and closing amounts from each year.

Merge all three years without missing any debtor.

Classify each debtor as:


1.Fully Paid

2.Partially Paid

3.Not Paid

4.Increased (New Credit Given)


Identify:

1.New debtors in 2024

2.New debtors in 2025

3.Generate a professional Excel output report.


**Technologies Used**

Python 3

Pandas

NumPy

OpenPyXL

Google Colab

**Input Files**

The project uses three Excel files:

2023.xlsx

2024.xlsx

2025.xlsx

Each file contains financial statements with a Sundry Debtors section.

**Methodology**

Data Extraction


**The program:**

1.Searches for the "Sundry Debtors" heading

2.Extracts all names listed below it

3.Captures the last numeric value in each row as the closing balance

4.Stops extraction at the "Total" line

5.Ensures no totals or unrelated headings are included


**Data Merging**

All three years are merged using an outer join to ensure:

1.No debtor is missed

2.Missing years are treated as zero balance

**Classification Logic**

Each debtor is classified based on year-by-year movement:

Condition	Classification
1.Amount becomes 0	Fully Paid
2.Amount decreases	Partially Paid
3.Amount remains same	Not Paid
4.Amount increases	Increased (New Credit Given)

**New Debtor Identification**

The system flags:

1.Debtors appearing in 2024 but not in 2023

2.Debtors appearing in 2025 but not in 2024

**Output**

The system generates:

Final_Sundry_Debtors_Analysis.xlsx

The Excel file contains:

Sheet: Analysis

| Debtor Name | Amount 2023 | Amount 2024 | Amount 2025 | Payment Status | New in 2024 | New in 2025 |

The file is professionally formatted with:

Title

Bold headings

Clean structure

**How to Run**

Upload Excel files to Google Colab.

Install required packages:

pip install openpyxl

Run the Python script.

Download the generated Excel file.

**Practical Applications**

This system can be used for:

Internship financial analysis

Accounting monitoring

Credit control tracking

Audit preparation

Year-over-year debtor analysis

**Accuracy Measures**

The script ensures:

1.No debtor names are skipped

2.No balances are missed

3.Totals are excluded

4.Missing years default to zero

5.Clean and reliable classification

**Conclusion**

This project demonstrates how Python can automate financial analysis tasks efficiently and accurately. It reduces manual checking errors and provides structured, professional output suitable for reporting and auditing purposes.
